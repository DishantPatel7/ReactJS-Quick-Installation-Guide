# React App Fast Installation Steps

# For Vite App + Tailwind

### Step 1 : create file

Link [--> Vite App Guide](https://vitejs.dev/guide/)

```
npm create vite@latest
```

### Step 2 : npm install

```
npm i

```

### Step 3 : Tailwind install

Link [--> Tailwind](https://tailwindcss.com/docs/guides/vite)

#### Paste in terminal

```
npm install -D tailwindcss postcss autoprefixer

```

```
npx tailwindcss init -p
```

### Step 4 : Add to tailwind.config.js file

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

```

### Step 5 : index.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Step 6 : Prettier Install

Link [-->Tailwind X Prettier](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier)

#### Paste in terminal

```
npm install -D prettier prettier-plugin-tailwindcss
```

### Step 7 : Create Prettier File

#### File Name .prettierrc.json

```
.prettierrc.json
```

#### Paste in the File

```
{
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### Step 8 : Open in VSCode

```
code .
```

### Step 9 : Start App

```
npm run dev
```
