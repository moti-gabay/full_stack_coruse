# Getting Started with Next.js

This guide takes you from zero to a Next.js app running on your machine, with 8 short exercises that cover the basics: pages, navigation, a client component, data fetching, a dynamic page, a form and an API.

Each exercise takes 5–15 minutes. Do them in order, in the same project.

---

## 1. Before you start

| What | Why | How to check |
| --- | --- | --- |
| Node.js 20.9 or later | Next.js runs on Node | `node -v` |
| npm (comes with Node) | Installs packages and runs scripts | `npm -v` |
| A code editor | VS Code is recommended | — |
| A terminal | Windows, macOS, Linux or WSL | — |

If `node -v` shows an older version, or the command isn't recognized, download the LTS version from [nodejs.org](https://nodejs.org/).

---

## 2. Create a project

In your terminal, in the folder where you want the project:

```bash
npx create-next-app@latest my-app
```

You'll see this question:

```txt
Would you like to use the recommended Next.js defaults?
    Yes, use recommended defaults
    No, reuse previous settings
    No, customize settings
```

Choose **Yes, use recommended defaults**. Here's what you get:

| Setting | What it means |
| --- | --- |
| TypeScript | Code is written in `.tsx` files, with types |
| ESLint | Checks your code and warns about mistakes |
| Tailwind CSS | Styling with classes like `p-4` and `text-blue-600` |
| App Router | Folder-based routing inside `app/` |
| Cache Components | Next.js’s new caching model |
| AGENTS.md | A file that helps AI tools write up-to-date Next.js code |

> **Tip:** to skip the questions and use the defaults right away: `npx create-next-app@latest my-app --yes`

---

## 3. Run it

```bash
cd my-app
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser. You should see the Next.js welcome page.

Any change you save in the code shows up in the browser immediately, without a refresh.

| Command | What it does |
| --- | --- |
| `npm run dev` | Development server with live reload (you’ll use this most of the time) |
| `npm run build` | Builds a production version |
| `npm run start` | Runs the production build |
| `npm run lint` | Checks your code with ESLint |

---

## 4. What’s in the folder

```txt
my-app/
├── app/
│   ├── layout.tsx      ← the shell around the whole site (html, body, menu)
│   ├── page.tsx        ← the home page, at /
│   └── globals.css     ← global styles and Tailwind
├── public/             ← images and static files, served from /
├── next.config.ts      ← Next.js settings
├── package.json        ← packages and scripts
├── tsconfig.json       ← TypeScript settings
└── AGENTS.md           ← instructions for AI tools
```

**The most important rule:** every folder inside `app/` that contains a `page.tsx` file is a URL on your site.

---

## 5. First exercises

### Exercise 1 · Change the home page

Replace everything in `app/page.tsx` with this:

```tsx
// app/page.tsx
export default function HomePage() {
  return (
    <main className="p-8">
      <h1 className="text-3xl font-bold">Hello, Next.js!</h1>
      <p className="mt-2 text-gray-600">This is my first project.</p>
    </main>
  );
}
```

Save, and the browser updates on its own.

---

### Exercise 2 · A new page

Create a folder called `about` inside `app`, with a `page.tsx` file in it:

```tsx
// app/about/page.tsx
export default function AboutPage() {
  return (
    <main className="p-8">
      <h1 className="text-3xl font-bold">About</h1>
      <p className="mt-2">This page lives at /about</p>
    </main>
  );
}
```

Go to [http://localhost:3000/about](http://localhost:3000/about). You didn’t define a route anywhere. You just created a folder.

---

### Exercise 3 · A navigation menu

In `app/layout.tsx`, add an `import` at the top of the file and a menu inside `<body>`, before `{children}`:

```tsx
// app/layout.tsx
import Link from "next/link";

// ... the rest of the existing code stays as it is

<body className={/* the className that's already there */}>
  <nav className="flex gap-4 border-b p-4">
    <Link href="/">Home</Link>
    <Link href="/about">About</Link>
    <Link href="/posts">Posts</Link>
    <Link href="/guestbook">Guestbook</Link>
  </nav>
  {children}
</body>
```

The menu appears on every page, because `layout.tsx` wraps all of them. `<Link>` navigates without reloading the page, unlike a regular `<a>` tag.

---

### Exercise 4 · A client component with state

In Next.js, every component runs on the server by default. When you need interaction (`useState`, `onClick`), add `"use client"` as the first line.

Create a `components` folder in the project root (next to `app`), with this file in it:

```tsx
// components/Counter.tsx
"use client";

import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button
      onClick={() => setCount(count + 1)}
      className="rounded bg-blue-600 px-4 py-2 text-white"
    >
      Clicked {count} times
    </button>
  );
}
```

And use it on the home page:

```tsx
// app/page.tsx
import Counter from "@/components/Counter";

export default function HomePage() {
  return (
    <main className="space-y-4 p-8">
      <h1 className="text-3xl font-bold">Hello, Next.js!</h1>
      <Counter />
    </main>
  );
}
```

> **Try it:** delete the `"use client"` line and save. You’ll get an error, because you can’t use `useState` in a server component. Put the line back.

`@/` is a shortcut for the project root, so you don’t have to write `../../`.

---

### Exercise 5 · Fetching data on the server

In a server component you can use `async` and `await` directly, with no `useEffect` and no loading state.

```tsx
// app/posts/page.tsx
import Link from "next/link";

type Post = { id: number; title: string };

export default async function PostsPage() {
  const res = await fetch("https://jsonplaceholder.typicode.com/posts?_limit=10");
  const posts: Post[] = await res.json();

  return (
    <main className="p-8">
      <h1 className="mb-4 text-3xl font-bold">Posts</h1>
      <ul className="space-y-2">
        {posts.map((post) => (
          <li key={post.id}>
            <Link href={`/posts/${post.id}`} className="text-blue-600 hover:underline">
              {post.title}
            </Link>
          </li>
        ))}
      </ul>
    </main>
  );
}
```

Add one more file in the same folder, shown while the data loads:

```tsx
// app/posts/loading.tsx
export default function Loading() {
  return <p className="p-8">Loading...</p>;
}
```

> **Why do you need `loading.tsx`?** The data comes from an external API at request time. Next.js needs to know what to show in the meantime, and `loading.tsx` is the answer. Without it you’ll get an error asking you to wrap the page in `<Suspense>`.

> **Try it:** open View Source (`Ctrl+U`). The post titles are already in the HTML, because the page was built on the server.

---

### Exercise 6 · A dynamic page

A folder named `[id]`, in square brackets, is a variable part of the URL: `/posts/1`, `/posts/2` and so on.

```tsx
// app/posts/[id]/page.tsx
import { notFound } from "next/navigation";

type Post = { id: number; title: string; body: string };

export default async function PostPage({
  params,
}: {
  params: Promise<{ id: string }>;
}) {
  const { id } = await params;
  const res = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`);

  if (!res.ok) notFound();

  const post: Post = await res.json();

  return (
    <main className="p-8">
      <h1 className="text-3xl font-bold">{post.title}</h1>
      <p className="mt-4 leading-relaxed">{post.body}</p>
    </main>
  );
}
```

Click a post in the list. Also try [http://localhost:3000/posts/999](http://localhost:3000/posts/999), which returns a 404 page.

> **Note:** `params` is a Promise, so you write `await params`. This is a common mistake for anyone coming from older versions of Next.js.

The `loading.tsx` from exercise 5 covers this page too, because it sits in the folder above it.

---

### Exercise 7 · A form with a Server Action

A Server Action is a function that runs on the server and is called directly from a form. No API, no `fetch`, no `onSubmit`.

Three files in the `app/guestbook` folder:

```ts
// app/guestbook/data.ts
export const messages: { id: number; text: string }[] = [];
```

```ts
// app/guestbook/actions.ts
"use server";

import { revalidatePath } from "next/cache";
import { messages } from "./data";

export async function addMessage(formData: FormData) {
  const text = String(formData.get("text") ?? "").trim();
  if (!text) return;

  messages.push({ id: Date.now(), text });
  revalidatePath("/guestbook");
}
```

```tsx
// app/guestbook/page.tsx
import { addMessage } from "./actions";
import { messages } from "./data";

export default function GuestbookPage() {
  return (
    <main className="space-y-4 p-8">
      <h1 className="text-3xl font-bold">Guestbook</h1>

      <form action={addMessage} className="flex gap-2">
        <input
          name="text"
          placeholder="Write something..."
          className="flex-1 rounded border px-3 py-2"
        />
        <button type="submit" className="rounded bg-blue-600 px-4 py-2 text-white">
          Add
        </button>
      </form>

      <ul className="space-y-1">
        {messages.map((m) => (
          <li key={m.id} className="rounded bg-gray-100 px-3 py-2">
            {m.text}
          </li>
        ))}
      </ul>
    </main>
  );
}
```

- `"use server"` marks the functions in the file as server-only.
- `revalidatePath` tells Next.js to rebuild the page, so the new message shows up.
- The messages are kept in the server’s memory and disappear when it restarts. Later in the course we’ll connect a real database.

---

### Exercise 8 · Your own API

A `route.ts` file creates an API URL that returns JSON, with no page.

```ts
// app/api/hello/route.ts
export async function GET() {
  return Response.json({ message: "Hello from Next.js" });
}
```

Go to [http://localhost:3000/api/hello](http://localhost:3000/api/hello).

> **API or Server Action?** A form inside your own site: Server Action. A URL that something outside calls (an app, another service): Route Handler.

---

## 6. What you built

| URL | File | What you learned |
| --- | --- | --- |
| `/` | `app/page.tsx` | A page, and a client component with `"use client"` |
| `/about` | `app/about/page.tsx` | Folder = URL |
| Every page | `app/layout.tsx` | A shared shell and `<Link>` |
| `/posts` | `app/posts/page.tsx` | `async` and `await` on the server, `loading.tsx` |
| `/posts/1` | `app/posts/[id]/page.tsx` | A dynamic page, `await params`, `notFound()` |
| `/guestbook` | `app/guestbook/page.tsx` | A form with a Server Action |
| `/api/hello` | `app/api/hello/route.ts` | A Route Handler that returns JSON |

---

## 7. Common problems at the start

| What you see | Why it happens | What to do |
| --- | --- | --- |
| An error about `useState` or `onClick` | The component is a server component | Add `"use client"` as the first line |
| An error asking for `<Suspense>` | The page fetches data at request time | Add a `loading.tsx` in the same folder |
| `params.id` is `undefined` | `params` is a Promise | `const { id } = await params` |
| The page doesn’t update after submitting a form | Next.js doesn’t know the data changed | `revalidatePath("/the-path")` at the end of the action |
| `Port 3000 is in use` | Another server is already running | Close it, or let Next.js switch to 3001 on its own |
| `npx` not recognized, or a version error | Node is missing or too old | Install Node LTS from nodejs.org |

---

## 8. Where to go next

- [Next.js docs](https://nextjs.org/docs): the most accurate and up-to-date source
- [Next.js Learn](https://nextjs.org/learn): a free official course that builds a full dashboard step by step
- [React docs](https://react.dev): for a refresher on hooks and state

> When you search Google or ask an AI, check that the answer fits the App Router and version 16. Many answers online still describe the Pages Router or older versions.
