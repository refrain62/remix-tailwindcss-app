# Remix + Tailwind CSS
https://tailwindcss.com/docs/guides/remix 

にならって作成

## プロジェクトの作成
```
npx create-remix@latest remix-tailwindcss-app
cd remix-tailwindcss-app
```

## Tailwind CSS の追加
```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init --ts -p
```

## tailwind.config.ts の調整
contentの内容を変更
```
import type { Config } from 'tailwindcss'

export default {
  content: ['./app/**/*.{js,jsx,ts,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
} satisfies Config
```

## tailswind CSSの追加
`./app/tailwind.css` のファイルを作成し設定
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## 開発開始
```
npm run dev
```

## トップページを変更してみる
`./app/routes/_index.ts` の内容を変更



# Welcome to Remix + Vite!

📖 See the [Remix docs](https://remix.run/docs) and the [Remix Vite docs](https://remix.run/docs/en/main/guides/vite) for details on supported features.

## Development

Run the Vite dev server:

```shellscript
npm run dev
```

## Deployment

First, build your app for production:

```sh
npm run build
```

Then run the app in production mode:

```sh
npm start
```

Now you'll need to pick a host to deploy it to.

### DIY

If you're familiar with deploying Node applications, the built-in Remix app server is production-ready.

Make sure to deploy the output of `npm run build`

- `build/server`
- `build/client`
