# Todo Workshop App

## Project Description
This is a beginner-friendly Todo App built with React and Vite. It demonstrates the basics of React, including state management with `useState`, event handling, and derived state. The app also integrates `localStorage` to persist tasks across page reloads. Styling is achieved using Tailwind CSS via a CDN for simplicity.

### Features
- Add, toggle, and delete tasks.
- Persistent storage using `localStorage`.
- Dynamic statistics: total tasks, completed tasks, and completion rate.
- Responsive design with Tailwind CSS.

This app is designed for workshops to introduce React concepts in a hands-on manner.

---

## Workshop Context
This project is designed for a hands-on workshop introducing React. Participants will learn how to:
- Set up a React project with Vite.
- Manage state using `useState`.
- Handle events and update the UI dynamically.
- Persist data using `localStorage`.
- Style components using Tailwind CSS.

By the end of the workshop, attendees will have a functional Todo App and a solid understanding of React fundamentals.

---

## Teaching Procedure: Build This App from Scratch

### 1. Set Up the Environment
1. **Install Node.js**: Ensure Node.js is installed on your system. Download it from [nodejs.org](https://nodejs.org).
2. **Initialize the Project**:
   ```bash
   mkdir todo-workshop
   cd todo-workshop
   npm init vite@latest
   # Choose React as the framework
   ```
3. **Install Dependencies**:
   ```bash
   npm install react react-dom lucide-react
   ```
4. **Install Dev Dependencies**:
   ```bash
   npm install vite --save-dev
   ```

### 2. Create the Project Files
1. **`index.html`**: Create the entry point for the app.
   ```html
   <!doctype html>
   <html lang="en">
     <head>
       <meta charset="utf-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Todo Workshop</title>
       <script src="https://cdn.tailwindcss.com"></script>
     </head>
     <body class="antialiased bg-orange-50 font-sans">
       <div id="root"></div>
       <script type="module" src="/src/main.jsx"></script>
     </body>
   </html>
   ```

2. **`src/main.jsx`**: Set up the React entry point.
   ```jsx
   import React from 'react';
   import { createRoot } from 'react-dom/client';
   import App from './App';
   import './index.css';

   const root = createRoot(document.getElementById('root'));
   root.render(<App />);
   ```

3. **`src/App.jsx`**: Build the Todo App component.
   - Start with a simple component that renders "Hello, World!".
   - Gradually add state (`useState`) for tasks.
   - Implement `addTask`, `toggleTask`, and `deleteTask` handlers.
   - Add derived state for statistics.
   - Integrate `localStorage` to persist tasks.

4. **`src/index.css`**: Add minimal base styles.
   ```css
   :root {
     --font-sans: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
   }

   html, body, #root {
     height: 100%;
   }

   body {
     margin: 0;
     font-family: var(--font-sans);
   }
   ```

### 3. Run the App
1. Start the development server:
   ```bash
   npm run dev
   ```
2. Open the app in your browser (usually at `http://localhost:5173`).

### 4. Explain Key Concepts
- **React Basics**: Explain `useState` and how state updates trigger re-renders.
- **Event Handling**: Show how `onClick` and `onChange` work.
- **Derived State**: Discuss how statistics are calculated from the `tasks` array.
- **Persistence**: Explain how `localStorage` is used to save and load tasks.
- **Styling**: Highlight the use of Tailwind CSS for rapid styling.

### 5. Build for Production
1. Build the app:
   ```bash
   npm run build
   ```
2. Preview the production build:
   ```bash
   npm run preview
   ```

---

## Notes for Students
- This app uses `Date.now()` for task IDs for simplicity. In production, consider using a library like `uuid`.
- Tailwind CSS is included via a CDN for simplicity. For production, set up a proper Tailwind build process.
- The app is intentionally simple to focus on React fundamentals. For advanced features, explore React Router, Context API, or state management libraries like Redux.
