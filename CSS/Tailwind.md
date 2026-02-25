
# Introduction to Tailwind CSS

## What is Tailwind?

Tailwind CSS is a utility-first CSS framework designed to enable users to create applications faster and easier. You can use utility classes to control the layout, color, spacing, typography, shadows, and more to create a completely custom component design — without leaving your HTML or writing a single line of custom CSS.

## What do we mean by "Utility-first"?

Utility-first is a CSS methodology where you build up your styles using many small, purpose-specific classes.

**Example comparison:**

**Before Tailwind (traditional CSS):**

```css
.btn {
  padding: 0.5em 1em;
  background-color: blue;
  color: white;
  border-radius: 0.25em;
}
```

**After Tailwind:**

```html
<button class="px-4 py-2 bg-blue-600 text-white rounded">Click me</button>
```

## Common Ways to Set Up Tailwind in Your Project

### Method 1: Tailwind via CDN (Quickest – No Installation)

1. Create an `index.html` file
2. Add this line inside the `<head>` tag:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

3. Start using Tailwind classes:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Tailwind Test</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 min-h-screen flex items-center justify-center">
  <h1 class="text-4xl font-bold text-blue-700">
    Hello Tailwind!
  </h1>
</body>
</html>
```

→ Best for: prototyping, quick demos, learning, or very small projects

### Method 2: Tailwind using CLI (Recommended for real projects)

**Step 1:** Initialize npm project

```bash
npm init -y
```

**Step 2:** Install Tailwind CSS

```bash
npm install -D tailwindcss
```

**Step 3:** Generate tailwind.config.js

```bash
npx tailwindcss init
```

**Step 4:** Create your input CSS file (e.g. `src/input.css`)

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

**Step 5:** Configure content paths in `tailwind.config.js`

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./*.html",
    "./src/**/*.{html,js}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

**Step 6:** Build & watch for changes

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

**Step 7:** Link the generated CSS in your HTML

```html
<link rel="stylesheet" href="/dist/output.css" />
```

For framework-specific setup (Vite, Next.js, React, Vue, Laravel, etc.)  
→ Official guide: https://tailwindcss.com/docs/installation

## Why Use Tailwind CSS?

1. **Utility-first approach**  
   Tailwind gives small ready-made classes instead of big fixed components.  
   Think of it like LEGO blocks — you combine small pieces to build any design you want.  
   You style directly in HTML, so you always know what style is applied where.

2. **Reusability and consistency**  
   Once you learn the classes, you can reuse the same styles everywhere.  
   This makes websites look consistent and saves time.

3. **Removes unused CSS (Purge feature)**  
   Tailwind automatically deletes unused styles from the final CSS file.  
   This keeps the website fast and lightweight.

4. **Less custom CSS**  
   Most styling is done using Tailwind classes, so you write very little custom CSS.  
   Code stays clean and easy to manage.

5. **Faster workflow**  
   No need to jump between HTML and CSS files.  
   You style directly inside HTML, which makes development quick and simple.

6. **Works with any framework**  
   Tailwind works well with React, Vue, Angular, Svelte, or plain HTML/JS.  
   You can use it in any project without problems.

7. **Active updates and strong community**  
   Tailwind is regularly updated and has a large, helpful community.  
   This keeps it modern, reliable, and well-supported.


