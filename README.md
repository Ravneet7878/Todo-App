# Todo-App

# **Todo App**  

This is a simple **Todo App** built with **React + Vite**, which allows users to efficiently manage their tasks. The application supports adding, updating, completing, and deleting todos while persisting data using **local storage**.  

---

## **Features**  
- ✅ **Add Todos**: Create new tasks effortlessly.  
- ✏️ **Edit Todos**: Modify existing tasks.  
- ✅ **Mark as Completed**: Track task progress with a checkbox.  
- ❌ **Delete Todos**: Remove completed or unnecessary tasks.  
- 💾 **Local Storage Support**: Tasks persist even after a page refresh.  
- ⚡ **Fast and Responsive UI**: Built using **Tailwind CSS**.  

---

## **Technologies Used**  
- 🟢 **React** – For building the UI.  
- ⚡ **Vite** – For fast development.  
- 🎨 **Tailwind CSS** – For styling.  
- 🌐 **Local Storage** – For persisting data.  

---

## **State Management with Context API**  

This project uses **React Context API** for managing the state globally. Instead of prop drilling, all todo-related functions and data are available via `useTodo()`.  

### **Todo Context (`TodoContext.js`)**  

```javascript
import { createContext, useContext } from "react";

export const TodoContext = createContext({
    todos: [],
    addTodo: () => {},
    updateTodo: () => {},
    deleteTodo: () => {},
    toggleComplete: () => {}
})

export const useTodo = () => {
    return useContext(TodoContext)
}

export const TodoProvider = TodoContext.Provider
```
