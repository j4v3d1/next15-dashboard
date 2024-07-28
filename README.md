This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/create-next-app).

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

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.


************************************************************************************************

npm install -g pnpm
pnpm create next-app@rc
pnpm dev


create file lib/constants.ts
//Paste in constants

export const SERVER_URL =
  process.env.NEXT_PUBLIC_SERVER_URL || 'http://localhost:3000'
export const APP_NAME = process.env.NEXT_PUBLIC_APP_NAME || 'NextAdmin'
export const APP_DESCRIPTION =
  process.env.NEXT_PUBLIC_APP_DESCRIPTION ||
  'An modern dashboard built with Next.js 15, Postgres, Shadcn'
export const ITEMS_PER_PAGE = Number(process.env.ITEMS_PER_PAGE) || 5


////Paste in .env.local

NEXT_PUBLIC_SERVER_URL=http://localhost:3000
NEXT_PUBLIC_APP_NAME=NextAdmin
NEXT_PUBLIC_APP_DESCRIPTION=Next.js 15 Dashboard
ITEMS_PER_PAGE=5

// create file components/shared/fonts.ts
               components/shared/fonts.ts
// paste into fonts.ts


import { Inter, Lusitana } from 'next/font/google'

export const inter = Inter({ subsets: ['latin'] })

export const lusitana = Lusitana({
  weight: ['400', '700'],
  subsets: ['latin'],
})


// goto layout.tsx
update layout.tsx

// goto create app-logo component
components/shared/app-logo.tsx

//add logo.png to public folder

// edit page.tsx in app folder


