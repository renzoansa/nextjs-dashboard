# Next.js Dashboard Project

- **Framework & Styling**:  
  Built using Next.js 15 with Tailwind CSS for styling and Google Fonts via `next/font/google` for optimal performance by preloading fonts at build time.

- **Streaming & Suspense**:  
  Implements streaming and the `Suspense` component with `loading.tsx` to display skeletons while chunks of pages are rendered in parallel. This enables efficient loading states during server-side data fetching and allows the app to progressively show content as it becomes available.

- **Server Components & Actions**:  
  Utilizes server components and `await` in server actions, allowing seamless server-side logic handling. Components with server actions include features like `bind` for encoding values, and form actions triggered via the `action` attribute.

- **Error Handling & Not Found Pages**:  
  Includes error boundary (`error.tsx`) for handling route-level errors with fallback UI, and a `not-found.tsx` page for resources that don’t exist using the `notFound` function from `next/navigation`.

- **State & Form Validation**:  
  Handles form errors using `useActionState` hook and validates forms with Zod. Uses `bcrypt` for password hashing and integrates `next-auth` for authentication and authorization.

- **Database & Asynchronous Operations**:  
  Connects to a PostgreSQL database using `@vercel/postgres`, with queries initiated in parallel via `Promise.all()` and `Promise.allSettled()` for efficient data fetching.

- **Routing & Layout**:  
  Supports dynamic routes with specific IDs and uses nested layouts shared across multiple dashboard pages. The dashboard root layout is prerendered, deferring dynamic content rendering until a user requests the route.

- **Navigation & Metadata**:  
  Uses the `Link` component for client-side navigation with background prefetching. Metadata is configured via an exported object, including the use of `title.template` to define dynamic page titles.

- **Client vs Server Components**:  
  `use client` directive is employed for client components (enabling hooks and event listeners), while `use server` is used to denote server actions.

- **Utility Hooks**:  
  Leverages `usePathname` and `useSearchParams` to read the current URL and search parameters in client components.
