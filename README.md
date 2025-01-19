## Step 1: Initialize a Node.js Project
```bash
npm init -y
```




## Step 2: Install Tailwind CSS 
```bash
npm i -D tailwindcss postcss autoprefixer
```




## Step 3: Create Tailwind Config File 
```bash
npx tailwindcss init
```
This creates a default tailwind.config.js file.
Modify it to specify which files Tailwind should scan:
```bash
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```




## Step 4: Add Tailwind to Your CSS
Create src/css/input.css and add:

```bash
@tailwind base;
@tailwind components;
@tailwind utilities;
```




## Step 5: Add a Build Script
Edit package.json and add this script:

```bash
"scripts": {
  "build": "npx tailwindcss -i ./src/css/input.css -o ./dist/output.css --watch"
}
```




## Step 6: Create index.html
Inside src/index.html:

```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tailwind CSS Project</title>
    <link href="../dist/output.css" rel="stylesheet">
</head>
<body class="bg-gray-100 text-center p-10">
    <h1 class="text-3xl font-bold text-blue-600">Hello, Tailwind CSS!</h1>
</body>
</html>
```




## Step 7: Build Tailwind CSS
```bash
npm run build
```



## Step 8: Start Development
To watch for changes automatically:

```bash
npm run build
```