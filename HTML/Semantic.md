# Semantic HTML: Writing Meaningful Web Pages

## What is Semantic HTML?

Semantic HTML uses HTML elements that describe the meaning of the content they contain. Instead of using only `<div>` and `<span>`, semantic tags like `<header>`, `<nav>`, `<article>`, and `<footer>` tell browsers and developers what the content is about.

The word "semantic" means "related to meaning." **Semantic HTML describes what content is, not only how it looks.**

## Why use Semantic HTML?

### 1. Better Accessibility

Screen readers and other assistive tools use semantic elements to help users move through a page. Using the right tags makes your site easier to use for people with disabilities.

### 2. Improved SEO

Search engines understand pages better when you use semantic elements. That can help with how your pages are indexed and found.

### 3. Easier Maintenance

Code that uses meaningful tags is easier to read and understand. Other developers (or you later) can see the page structure quickly.

### 4. Consistent Structure

Semantic elements give a standard way to organize content. This helps teams work together and keeps the site predictable.

---

## Common Semantic HTML Elements

### `<header>`

Represents introductory content or navigation. Often contains the site title or main menu.

```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>
```

**Use for:** site headers, top-of-page navigation, article headers.

---

### `<nav>`

Contains navigation links. Use this for menus and major navigation lists.

```html
<nav>
  <ul>
    <li><a href="/home">Home</a></li>
    <li><a href="/blog">Blog</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>
</nav>
```

**Use for:** main menus, table of contents, breadcrumbs.

---

### `<main>`

The main content of the page. There should be only one `<main>` per page and it should contain the primary content unique to that page.

```html
<main>
  <h1>Welcome to My Blog</h1>
  <p>This is the main content area.</p>
</main>
```

**Use for:** the primary content of the page.

---

### `<article>`

A self-contained piece of content that could stand alone, such as a blog post or news item.

```html
<article>
  <h2>How to Learn HTML</h2>
  <p>Published on January 15, 2024</p>
  <p>Learning HTML is the first step in web development...</p>
</article>
```

**Use for:** blog posts, news articles, forum posts, product cards.

---

### `<section>`

Groups related content. Use it for logical divisions within a page or article.

```html
<section>
  <h2>Our Services</h2>
  <p>We offer web design and development.</p>
</section>
```

**Use for:** chapters, topic groups, parts of an article.

---

### `<aside>`

Content related to but separate from the main content, like sidebars, related links, or author notes.

```html
<aside>
  <h3>Related Articles</h3>
  <ul>
    <li><a href="/css-basics">CSS Basics</a></li>
    <li><a href="/javascript-intro">JavaScript Intro</a></li>
  </ul>
</aside>
```

**Use for:** sidebars, author bio, related links.

---

### `<footer>`

Footer for a page or section. Often contains copyright, contact info, or extra navigation.

```html
<footer>
  <p>&copy; 2024 My Website. All rights reserved.</p>
  <nav>
    <a href="/privacy">Privacy Policy</a>
    <a href="/terms">Terms of Service</a>
  </nav>
</footer>
```

**Use for:** page footers, article footers, metadata.

---

## Before and After: Non-Semantic vs Semantic

### Non-semantic Example (less clear)

```html
<div class="header">
  <div class="logo">My Website</div>
  <div class="menu">
    <a href="#home">Home</a>
    <a href="#about">About</a>
  </div>
</div>

<div class="content">
  <div class="post">
    <div class="title">My First Blog Post</div>
    <div class="text">This is my blog post content...</div>
  </div>
</div>

<div class="footer">
  <div class="copyright">© 2024</div>
</div>
```

**Problems:**
- Tags do not describe the content
- Assistive tools cannot identify structure easily
- The page depends on CSS class names for meaning

### Semantic Example (clearer)

```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
  </nav>
</header>

<main>
  <article>
    <h2>My First Blog Post</h2>
    <p>This is my blog post content...</p>
  </article>
</main>

<footer>
  <p>&copy; 2024</p>
</footer>
```

**Benefits:**
- Structure is clear to readers and machines
- Screen readers can navigate the page better
- Search engines can interpret the hierarchy

---

## Complete Page Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Blog - Semantic HTML Example</title>
</head>
<body>

  <header>
    <h1>My Personal Blog</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <article>
      <header>
        <h2>Understanding Semantic HTML</h2>
        <p>Published on <time datetime="2024-01-15">January 15, 2024</time></p>
        <p>By <strong>Jane Doe</strong></p>
      </header>

      <section>
        <h3>Introduction</h3>
        <p>Semantic HTML helps make web pages more understandable and accessible.</p>
      </section>

      <section>
        <h3>Why It Matters</h3>
        <p>Using semantic elements improves accessibility, search indexing, and code quality.</p>
      </section>

      <footer>
        <p>Tags: #HTML #WebDev #Accessibility</p>
      </footer>
    </article>

    <aside>
      <h3>About the Author</h3>
      <p>Jane is a web developer focused on accessibility and clear code.</p>

      <h3>Related Posts</h3>
      <ul>
        <li><a href="/css-basics">CSS Basics</a></li>
        <li><a href="/javascript-intro">Intro to JavaScript</a></li>
      </ul>
    </aside>
  </main>

  <footer>
    <p>&copy; 2024 My Blog. All rights reserved.</p>
    <nav>
      <a href="/privacy">Privacy Policy</a> |
      <a href="/terms">Terms of Service</a>
    </nav>
  </footer>

</body>
</html>
```

---

## Visual Structure

### Basic Layout

Here's how semantic elements typically organize a page:

```
┌─────────────────────────────────────┐
│          <header>                   │
│  ┌──────────────────────────────┐   │
│  │         <nav>                │   │
│  └──────────────────────────────┘   │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│           <main>                    │
│  ┌──────────────────┐  ┌─────────┐  │
│  │   <article>      │  │ <aside> │  │
│  │  ┌────────────┐  │  │         │  │
│  │  │ <section>  │  │  │         │  │
│  │  └────────────┘  │  │         │  │
│  │  ┌────────────┐  │  │         │  │
│  │  │ <section>  │  │  │         │  │
│  │  └────────────┘  │  │         │  │
│  └──────────────────┘  └─────────┘  │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│          <footer>                   │
└─────────────────────────────────────┘
```
