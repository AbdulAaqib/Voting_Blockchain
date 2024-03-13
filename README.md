---
import Base from "../layout/Base.astro";
import { supabase } from "../lib/supabase";
import { Reviews, type GuestbookEntry } from "../components/Reviews";

const { email } = Astro.locals;

const { data } = (await supabase
  .from("guestbook")
  .select("name, message")
  .order("created_at", { ascending: false })) as { data: GuestbookEntry[] };
---

<Base title="Dashboard">
  <Base title="Dashboard">
    <html lang="en">
  
  <head>
      <meta charset="UTF-8">
      <meta http-equiv="X-UA-Compatible" content="IE=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Voting App</title>
      <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
      <style>
          body {
              font-family: Arial, sans-serif;
          }
      </style>
  </head>
  
  <body class="bg-gray-200 p-4">
      <div class="max-w-md mx-auto bg-white p-6 rounded-md shadow-md">
          <h1 class="text-2xl font-bold mb-4">Vote for your favorite party</h1>
          <div class="grid grid-cols-2 gap-4">
              <button class="bg-blue-500 text-white py-2 px-4 rounded-md party">Party A</button>
              <button class="bg-red-500 text-white py-2 px-4 rounded-md party">Party B</button>
              <button class="bg-green-500 text-white py-2 px-4 rounded-md party">Party C</button>
              <button class="bg-yellow-500 text-white py-2 px-4 rounded-md party">Party D</button>
              <button class="bg-pink-500 text-white py-2 px-4 rounded-md party">Party E</button>
              <button class="bg-indigo-500 text-white py-2 px-4 rounded-md party">Party F</button>
              <button class="bg-purple-500 text-white py-2 px-4 rounded-md party">Party G</button>
              <button class="bg-gray-500 text-white py-2 px-4 rounded-md party">Party H</button>
              <button class="bg-orange-500 text-white py-2 px-4 rounded-md party">Party I</button>
              <button class="bg-teal-500 text-white py-2 px-4 rounded-md party">Party J</button>
          </div>
      </div>
  
      <a
        href="/api/auth/signout"
        class="mt-8 mb-4 bg-zinc-900 dark:bg-zinc-100 text-zinc-100 dark:text-zinc-900 px-3 py-1 rounded-md inline-block"
      >Sign out</a>
  
      <script>
          const partyButtons = document.querySelectorAll('.party');
  
          partyButtons.forEach((button) => {
              button.addEventListener('click', () => {
                  alert("Thank you for your vote!");
              });
          });
      </script>
  </body>
  
  </html>
  </Base>
  
</Base>


This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
