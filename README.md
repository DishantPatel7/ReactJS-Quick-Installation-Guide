# React App Fast Installation Steps

# For Vite App + Tailwind

### **Step 1 : create file**

`Link` --> [ Vite App Guide](https://vitejs.dev/guide/)

```
npm create vite@latest
```

```
npm i
```

### **Step 2 : Tailwind install**

`Link` --> [Tailwind](https://tailwindcss.com/docs/guides/vite)

`Paste in terminal`

```
npm install -D tailwindcss postcss autoprefixer
```

```
npx tailwindcss init -p
```

`Add to tailwind.config.js file`

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

`Add to index.css`

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### **Step 3 : Prettier Install**

Link [-->Tailwind X Prettier](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier)

`Paste in terminal`

```
npm install -D prettier prettier-plugin-tailwindcss
```

### Create Prettier File

`File Name .prettierrc.json`

```
.prettierrc.json
```

`Paste in the File`

```
{
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### **Step 4 : Open in VSCode**

```
code .
```

### **Step 5 : Start the App**

```
npm run dev
```

# Also Install library below

### 1. Framer Motion
`Link` --> [Framer Motion](https://www.framer.com/motion/introduction/)
#### Install
```
npm i framer-motion
```
#### Import
```
import { motion } from "framer-motion"
```

### 2. React Icon
`Link` --> [React-Icon](https://react-icons.github.io/react-icons/)
#### Install
```
npm i react-icons --save
```
