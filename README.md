## Next JS Framework By Qomunal

### Contribute

#### CEO

- Prasma Anindita

#### Programmer

- Muhammad Hafidz
- Faisal Amir

## Catatan Penting Sebelum Mulai

### Sebelum download

- Usahakan siapkan Node Module terlebih dahulu di PC / Laptop
- Gunakaan Node Version LTS

### Setelah download / clone dari github

- Jalankan npm install untuk mendownload Node modules yang ketinggalan

```bash
npm install
```

📦 Ini akan:

- Download semua dependency
- Generate ulang folder node_modules

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

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

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Notes Penting tapi Ga penting

### Beda file extension ts dan tsx

#### (1). .ts (TypeScript)

Dipakai untuk logic murni, tanpa JSX. Cocok untuk:

- util / helper
- service
- API client
- Redux / Zustand store
- backend (Node.js)

```ts
type User = {
  id: number;
  name: string;
};

function getUserName(user: User): string {
  return user.name;
}
```

#### (2). .tsx (TypeScript + JSX)

- Dipakai kalau file tersebut mengandung JSX / React component.
- JSX (<h1>...</h1>) tidak bisa ditulis di file .ts.

```tsx
type Props = {
  name: string;
};

const Hello = ({ name }: Props) => {
  return <h1>Hello {name}</h1>;
};

export default Hello;
```

#### (3). Aturan Praktis (Best Practice)

| Kondisi                   | Pakai  |
| ------------------------- | ------ |
| Tidak ada JSX             | `.ts`  |
| Ada JSX / React Component | `.tsx` |

Di Next.js / React:

- utils.ts
- services.ts
- types.ts
- components/Button.tsx
- pages/index.tsx

#### (4). Kalo Ada Error

Kalau JSX ditulis di .ts, akan error seperti:

```bash
Cannot use JSX unless the '--jsx' flag is provided
```

## Catatan Bawaan Dari Next JS

### Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

### Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
