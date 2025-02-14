# **Todo App**

This is a simple **Todo App** built with **React**, allowing users to add, update, delete, and mark tasks as completed. The application uses **Context API** for state management and **Local Storage** to persist todos.

## **Features:**
- ✅ **Add Todos**: Create new tasks effortlessly.
- ✏️ **Edit Todos**: Modify existing tasks.
- ✅ **Mark as Completed**: Track task progress with a checkbox.
- ❌ **Delete Todos**: Remove completed or unnecessary tasks.
- 💾 **Local Storage Support**: Tasks persist even after a page refresh.
- ⚡ **Fast and Responsive UI**: Built using Tailwind CSS.

## **Hooks Used in the Project:**

### **1. useState:**
`useState` is used to manage the state of todos and input fields.

**Usage in this project:**
- `todos`: Stores the list of todo items.
- `todo`: Stores the input value for adding a new todo.
- `isTodoEditable`: Tracks whether a todo is being edited.
- `todoMsg`: Stores the modified todo message when editing.

**Benefits:**
- Enables dynamic updates to the UI.
- Ensures state consistency throughout user interactions.

### **2. useEffect:**
`useEffect` is used for handling side effects such as local storage updates.

**Usage in this project:**
- Loads todos from `localStorage` when the app initializes.
- Saves todos to `localStorage` whenever the todo list updates.

**Benefits:**
- Ensures data persistence between page reloads.
- Reduces unnecessary re-renders by running only when dependencies change.

### **3. useContext:**
`useContext` is used to manage and share the todo state across components.

**Usage in this project:**
- Provides the todo state and functions (`addTodo`, `updateTodo`, `deleteTodo`, `toggleComplete`) via `TodoContext`.
- Consumed by `TodoForm` and `TodoItem` components to interact with the todo list.

**Benefits:**
- Avoids prop drilling by making state available globally.
- Improves code readability and maintainability.

## **Context API - TodoContext:**
A global context is created to manage todos efficiently.

```javascript
import { createContext, useContext } from "react"

export const TodoContext = createContext({
    todos : [],
    addTodo : () => {},
    updateTodo : () => {},
    deleteTodo : () => {},
    toggleComplete : () => {}
})

export const useTodo = () => useContext(TodoContext)
export const TodoProvider = TodoContext.Provider
```

## **Components in the Project:**

### **1. App Component**
Handles the main logic of the todo app, including state management and rendering todos.

### **2. TodoForm Component**
Allows users to add new todos using an input field and submit button.

### **3. TodoItem Component**
Displays individual todo items with options to edit, delete, and mark as completed.

## **Technologies Used:**
- 🟢 **React** – For building the UI.
- ⚡ **Vite** – For fast development.
- 🎨 **Tailwind CSS** – For styling.
- 🌐 **Local Storage** – For persisting data.
