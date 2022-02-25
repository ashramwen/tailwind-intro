---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## An introduction to Tailwind CSS
  Presentation slides for developers.

  Learn more at [Tailwindcss.TW](https://tailwindcss.tw/)
# persist drawings in exports and build
drawings:
  persist: false
---

# Introduction to Tailwind CSS

My personal favorite design framework

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/tailwindlabs/tailwindcss" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---

# Navigation

Hover on the bottom-left corner to see the navigation's controls panel

### Keyboard Shortcuts

|                                                       |                             |
| ----------------------------------------------------- | --------------------------- |
| <kbd>right</kbd> / <kbd>space</kbd>                   | next animation or slide     |
| <kbd>left</kbd> / <kbd>shift</kbd> + <kbd>space</kbd> | previous animation or slide |
| <kbd>up</kbd>                                         | previous slide              |
| <kbd>down</kbd>                                       | next slide                  |

<img
  v-click
  class="absolute -bottom-9 -left-7 w-80 opacity-50"
  src="https://sli.dev/assets/arrow-bottom-left.svg"
/>

<p v-after class="absolute bottom-23 left-45 opacity-30 transform -rotate-10">Here!</p>

---

# What is Tailwind CSS?

TailwindCSS is a CSS framework for developers, consist of the following features

- 📝 **Utility-first** - CSS packed with classes that can be composed to build any design
- ⚡ **Performance** - Tiny, never ship unused CSS
- 📱 **Responsive Design** - Adapt to any screen size using responsive modifiers
- 🌟 **State variants** - `hover`, `focus`, and other states? Got ’em
- ⚛️ **Reusing styles** - No need to be worried about duplication
- 🎨 **Themable** - Now with Dark Mode
- 🛠 **Customization** - Extend it, tweak it, change it

<br>
<br>

Read more about [Tailwind CSS](https://tailwindcss.tw/)

---

# Sizing

<div grid="~ cols-2 gap-4">
  <div>

```html
<div class="space-y-4">
  <div class="w-96 bg-white shadow rounded">w-96</div>
  <div class="w-80 bg-white shadow rounded">w-80</div>
  <div class="w-72 bg-white shadow rounded">w-72</div>
  <div class="w-64 bg-white shadow rounded">w-64</div>
  <div class="w-60 bg-white shadow rounded">w-60</div>
  <div class="w-56 bg-white shadow rounded">w-56</div>
  <div class="w-52 bg-white shadow rounded">w-52</div>
  <div class="w-48 bg-white shadow rounded">w-48</div>
</div>
```

</div>

<div>
  <Sizing />
</div>
</div>

<style>

</style>

---

# Colors

<div grid="~ cols-2 gap-4">
  <div>

```html
<div class="grid grid-cols-10 gap-2">
  <div class="bg-sky-50 aspect-square"></div>
  <div class="bg-sky-100 aspect-square"></div>
  <div class="bg-sky-200 aspect-square"></div>
  ...
  <div class="bg-sky-700 aspect-square"></div>
  <div class="bg-sky-800 aspect-square"></div>
  <div class="bg-sky-900 aspect-square"></div>
</div>

<div class="grid grid-cols-10 gap-2">
  <div class="bg-violet-50 aspect-square"></div>
  <div class="bg-violet-100 aspect-square"></div>
  <div class="bg-violet-200 aspect-square"></div>
  ...
  <div class="bg-violet-700 aspect-square"></div>
  <div class="bg-violet-800 aspect-square"></div>
  <div class="bg-violet-900 aspect-square"></div>
</div>
```

</div>

<div>
  <Colors />
</div>
</div>

<style>

</style>

---

# Shadows

<div grid="~ cols-2 gap-4">
  <div>

```html
<div class="grid grid-cols-2 gap-6">
  <div class="shadow-sm bg-white rounded-lg">
    shadow-sm
  </div>
  <div class="shadow bg-white rounded-lg">
    shadow
  </div>
  <div class="shadow-md bg-white rounded-lg">
    shadow-md
  </div>
  <div class="shadow-lg bg-white rounded-lg">
    shadow-lg
  </div>
  <div class="shadow-xl bg-white rounded-lg">
    shadow-xl
  </div>
  <div class="shadow-2xl bg-white rounded-lg">
    shadow-2xl
  </div>
</div>
```

</div>

<div>
  <Shadows />
</div>
</div>

<style>

</style>

---

# Installation

<div class="text-2xl">
- Use Tailwind CLI

<div v-click class="text-xl ml-4 text-gray-400">

    - The simplest way

</div>

</div>
<br/>
<div class="text-2xl">
- PostCSS plugin

<div v-click class="text-xl ml-4 text-gray-400">

    - Integrating it with build tools

</div>
<br/>
</div>

<div class="text-2xl">
- With frameworks

<div v-click class="text-xl ml-4 text-gray-400">

    - Supporting a number of popular frameworks

</div>
<br/>
</div>

<div class="text-2xl">
- Use CDN

<div v-click class="text-xl ml-4 text-gray-400">

    - Trying Tailwind right in the browser without any build step

</div>

</div>

<br>
<br>

<div v-click>

[Learn more](https://tailwindcss.tw/docs/installation)

</div>

---

# Frameworks support

<img src="/framework.png" alt="" />

---

# CDN

Use the Play CDN to try Tailwind right in the browser without any build step.

The Play CDN is designed for development purposes only, and is not the best choice for production.

```html {all|6,9-11}
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

---

# Editor support

- [Tailwind CSS IntelliSense for VS Code](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)  (Strongly recommend)
  - Autocomplete
  - Linting
  - Hover preview
  - Syntax highlighting

- Automatic Class Sorting with Prettier

```sh
> npm install -D prettier prettier-plugin-tailwindcss
```

- [WebStorm support](https://www.jetbrains.com/help/webstorm/tailwind-css.html)

- [PostCSS Language Support](https://marketplace.visualstudio.com/items?itemName=csstools.postcss)

---

# Custom CSS

Use `@apply` to inline any existing utility classes into your own custom CSS.

```css
.select2-dropdown {
  @apply rounded-b-lg shadow-md;
}
.select2-search {
  @apply border border-gray-300 rounded;
}
.select2-results__group {
  @apply text-lg font-bold text-gray-900;
}
```

<v-click>

```css
.foo {
  color: blue !important;
}

.bar {
  @apply foo;
}
```


[Learn more](https://tailwindcss.com/docs/functions-and-directives)

</v-click>

---

# Handling Hover, Focus, and Other States
Using utilities to style elements on hover, focus, and more.

<Hover />

```html
<button class="bg-violet-400
               hover:bg-violet-600
               active:bg-violet-900
               focus:outline-none focus:ring focus:ring-violet-300 ...">
  Save
</button>
```

<br>
<br>

<arrow v-click="1" x1="350" y1="130" x2="200" y2="143" color="#38E" width="3" arrowSize="1" />
<p v-after="1" class="absolute top-28 left-80 opacity-30 transform -rotate-10">Hover and click me!</p>

<v-click>

- **Pseudo-classes**, like `:hover`, `:focus`, `:first-child`, and `:required`
- **Pseudo-elements**, like `::before`, `::after`, `::placeholder`, and `::selection`
- **Media queries**, like responsive breakpoints, dark mode, and `prefers-reduced-motion`
- **Attribute selectors**, like `[dir="rtl"]` and `[open]`

</v-click>

---

# Responsive Design
By default, Tailwind uses a mobile first breakpoint system

<div>

| Breakpoint prefix      | Minimum width | CSS |
| ----------- | ----------- | --- |
| `sm`   | 640px       | `@media (min-width: 640px) { ... }` |
| `md`   | 768px        | `@media (min-width: 768px) { ... }` |
| `lg`   | 1024px        | `@media (min-width: 1024px) { ... }` |
| `xl`   | 1280px        | `@media (min-width: 1280px) { ... }` |
| `2xl`   | 1536px        | `@media (min-width: 1536px) { ... }` |

</div>

<br>

<div v-click>

```html
<!-- Width of 16 by default, 32 on medium screens, and 48 on large screens -->
<img class="w-16 md:w-32 lg:w-48" src="..." />
```

</div>

---


# Customize

<div grid="~ cols-2 gap-4">

<div>

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        brown: {
          50: '#fdf8f6',
          100: '#f2e8e5',
          200: '#eaddd7',
          300: '#e0cec7',
          400: '#d2bab0',
          500: '#bfa094',
          600: '#a18072',
          700: '#977669',
          800: '#846358',
          900: '#43302b',
        },
      }
    },
  },
}
```

</div>

<div>


<div v-click>

```js
module.exports = {
  theme: {
    extend: {
      screens: {
        sm: '480px',
        md: '768px',
        lg: '976px',
        xl: '1440px',
      },
      colors: {
        'blue': '#1fb6ff',
        'pink': '#ff49db',
        'orange': '#ff7849',
        'green': '#13ce66',
        'gray-dark': '#273444',
        'gray': '#8492a6',
        'gray-light': '#d3dce6',
      }
    }
  }
}
```

</div>

</div>

</div>

[Learn more](https://tailwindcss.com/docs/configuration)

---

# Resources

- [Official Tailwind UI](https://tailwindui.com/)
- [Headless UI](https://headlessui.dev/) (Free)
- [Tailwind Components](https://tailwindcomponents.com/) (Free)
- [Hero Patterns](https://heropatterns.com/) (Free)
- [Playground](https://play.tailwindcss.com/)

---
layout: center
class: text-center

---

# Q & A

[Tailwindcss.TW](https://tailwindcss.tw/) · [Slides](https://ashramwen.github.io/tailwind-intro/) · [community](https://www.facebook.com/groups/840139126924653)

