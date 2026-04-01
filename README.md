# ✓ Tasks — A Minimal Todo App

A lightweight, zero-dependency todo list app built with plain HTML, CSS, and JavaScript. No build tools, no frameworks, no setup — just open `index.html` and go.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![No dependencies](https://img.shields.io/badge/dependencies-none-brightgreen?style=flat)

---

## Features

- **Add tasks** with a name, category, and priority level
- **Category tags** — Personal, Work, or Health
- **Priority levels** — High, Medium, or Low (colour-coded dots)
- **Check off tasks** with an animated circular checkbox
- **Filter view** — switch between All, Active, and Done
- **Progress bar** — live percentage of tasks completed
- **Delete tasks** — hover a task to reveal the remove button
- **Clear completed** — bulk-remove all done tasks in one click
- **Live date header** — shows the current day automatically
- **Slide-in animations** on new task entries
- **Keyboard support** — press `Enter` to add a task

---

## Getting Started

No installation or build step required.

```bash
git clone https://github.com/your-username/tasks-todo-app.git
cd tasks-todo-app
open index.html
```

Or just download `index.html` and open it directly in any modern browser.

---

## Usage

1. Type a task name in the input field
2. Choose a **category** (Personal / Work / Health) and **priority** (High / Med / Low)
3. Press **Add task** or hit `Enter`
4. Click the circle on the left to mark a task complete
5. Hover a task and click **×** to delete it
6. Use the **All / Active / Done** filter tabs to switch views
7. Click **Clear completed** to remove all finished tasks at once

---

## Project Structure

```
tasks-todo-app/
└── index.html      # Entire app — HTML, CSS, and JS in one file
```

Everything lives in a single self-contained file. Styles are written with CSS custom properties for easy theming, and all logic is vanilla JavaScript with no external runtime dependencies (only the DM Sans and DM Serif Display fonts are loaded from Google Fonts).

---

## Customisation

### Changing the colour accent

Open `index.html` and update the `--accent` variable in `:root`:

```css
:root {
  --accent: #c84b2f; /* change this to any colour */
}
```

### Adding a new category

In the HTML, add an `<option>` to the `#cat-select` dropdown:

```html
<option value="learning">Learning</option>
```

Then add a matching CSS rule:

```css
.tag-learning { background: #e4eaf0; color: #162d54; }
```

### Persisting tasks across page reloads

The app stores tasks in memory only. To persist them, wrap the `tasks` array with `localStorage`:

```js
// Load
let tasks = JSON.parse(localStorage.getItem('tasks') || '[]');

// Save (call after every mutation)
function save() {
  localStorage.setItem('tasks', JSON.stringify(tasks));
}
```

---

## Browser Support

Works in all modern browsers — Chrome, Firefox, Safari, and Edge. No polyfills needed.

---

## License

MIT — free to use, modify, and distribute.
