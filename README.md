# React App Fast Installation Steps

# For Vite App + Tailwind

### **Step 1 : create file**

Link [--> Vite App Guide](https://vitejs.dev/guide/)

```
npm create vite@latest
```

```
npm i
```

### **Step 2 : Tailwind install**

Link [--> Tailwind](https://tailwindcss.com/docs/guides/vite)

#### Paste in terminal

```
npm install -D tailwindcss postcss autoprefixer
```

```
npx tailwindcss init -p
```

#### Add to tailwind.config.js file

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

#### Add to index.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### **Step 3 : Prettier Install**

Link [-->Tailwind X Prettier](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier)

#### Paste in terminal

```
npm install -D prettier prettier-plugin-tailwindcss
```

#### Create Prettier File

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

### **Step 4 : Open in VSCode**

```
code .
```

### **Step 5 : Start the App**

```
npm run dev
```

# Vite App Upload On Git Page

### **Step 1 : Go to vite.config.js**
```
base:"/Repository-name",
```

### **Step 2 : Go to Setting(GitHub Website)**

#### --> Open Pages

#### --> Build and deployment

#### --> Source

#### --> Select "GitHub Actions"

#### --> Click on "create your own"

### **Step 3 : Create deploy.yml file**

```
deploy.yml
```

#### Copy code and paste into deploy.yml

```
# Simple workflow for deploying static content to GitHub Pages
name: Deploy static content to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ['main']

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets the GITHUB_TOKEN permissions to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow one concurrent deployment
concurrency:
  group: 'pages'
  cancel-in-progress: true

jobs:
  # Single deploy job since we're just deploying
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Set up Node
        uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'npm'
      - name: Install dependencies
        run: npm ci
      - name: Build
        run: npm run build
      - name: Setup Pages
        uses: actions/configure-pages@v4
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          # Upload dist folder
          path: './dist'
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

