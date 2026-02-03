# React Router SPA Experiments
A collection of React Single Page Application (SPA) experiments built using React Router.  
This repository demonstrates core routing concepts including navigation, component mapping, and multi-page SPA architecture.
These experiments were developed as part of a practical lab to understand modern client-side routing in React.

---

## 🚀 Experiments Overview

### 🔹 Experiment 1 — Basic Client-Side Routing
**Objective:**  
Implement basic routing inside a React SPA.

**Summary:**  
This experiment introduces React Router fundamentals by mapping different components to routes. It demonstrates how navigation occurs without reloading the page.

**Key Concepts:**
- BrowserRouter setup
- Routes & Route mapping
- Component-based navigation
- SPA behavior

<img width="1161" height="524" alt="image" src="https://github.com/user-attachments/assets/9fb86860-a37e-490b-bf1f-e60c3e16eb35" />
<img width="934" height="471" alt="image" src="https://github.com/user-attachments/assets/ddd90f1c-7ac9-4771-b8bf-81a2902fffe3" />
<img width="912" height="447" alt="image" src="https://github.com/user-attachments/assets/90b584ca-70a2-4e32-a4ce-b63e6546856c" />

---

### 🔹 Experiment 2 — Navigation Using Link Component
**Objective:**  
Implement user navigation using the Link component.

**Summary:**  
Focuses on smooth client-side navigation. Users can switch pages using navigation links without full page reload.

**Key Concepts:**
- Link component usage
- Navigation bar UI
- Smooth transitions
- Client-side routing

<img width="1896" height="755" alt="image" src="https://github.com/user-attachments/assets/33824f37-31fb-425c-af08-9d6cf13124f8" />
<img width="1892" height="713" alt="image" src="https://github.com/user-attachments/assets/412c0763-749d-459c-9a84-b03edd1846be" />

---

### 🔹 Experiment 3 — Multi-Page SPA Using Routing
**Objective:**  
Build a structured multi-page React application.

**Summary:**  
Creates a dashboard and profile system using modular components. Demonstrates real-world SPA structure and routing architecture.

**Key Concepts:**
- Multi-page SPA layout
- Component separation
- Dashboard/Profile routing
- Portfolio-style UI

<img width="1853" height="853" alt="image" src="https://github.com/user-attachments/assets/f315bc1c-25e3-48eb-a09b-0a58041c2023" />

![Experiment 3 Profile Demo](https://github.com/user-attachments/assets/c197cfc7-9e29-4e68-bbf0-78814de547a2)

---

## 🛠 Tech Stack
- React
- React Router DOM (v6+)
- Vite
- JavaScript (ES6+)
- CSS

---

## 🔧 Common Issues & Solutions

### ⚠️ Error: "A `<Route>` is only ever to be used as the child of `<Routes>` element"

**Problem:**  
This error occurs when `<Route>` components are not wrapped inside a `<Routes>` component, which is required in React Router v6+.

**Solution:**  
Always wrap your `<Route>` components inside a `<Routes>` wrapper.

#### ❌ Incorrect Code:
```jsx
<BrowserRouter>
  <Route path="/" element={<Home />} />
  <Route path="/about" element={<About />} />
  <Route path="/contact" element={<Contact />} />
</BrowserRouter>
```

#### ✅ Correct Code:
```jsx
<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
    <Route path="/contact" element={<Contact />} />
  </Routes>
</BrowserRouter>
```

#### 📝 Complete Working Example:
```jsx
import { BrowserRouter, Routes, Route, Link } from 'react-router-dom';
import Home from './components/Home';
import About from './components/About';
import Contact from './components/Contact';

function App() {
  return (
    <BrowserRouter>
      <nav>
        <Link to="/">Home</Link>
        <Link to="/about">About</Link>
        <Link to="/contact">Contact</Link>
      </nav>
      
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </BrowserRouter>
  );
}

export default App;
```

**Key Points:**
- In React Router v6+, `<Routes>` replaced the old `<Switch>` component from v5
- All `<Route>` components must be direct children of `<Routes>`
- Navigation components like `<Link>` should be placed outside `<Routes>`
- The `<Routes>` component handles route matching and rendering

---

## 📦 Installation

```bash
# Clone the repository
git clone <repository-url>

# Navigate to project directory
cd react-router-spa-experiments

# Install dependencies
npm install

# Run the development server
npm run dev
```

---

## 📚 Learning Resources
- [React Router Official Documentation](https://reactrouter.com/)
- [React Router v6 Migration Guide](https://reactrouter.com/en/main/upgrading/v5)
- [Vite Documentation](https://vitejs.dev/)

---

## 🤝 Contributing
Feel free to fork this repository and submit pull requests for improvements or additional experiments.

---

## 📄 License
This project is open source and available for educational purposes.

---

**Happy Routing! 🚀**
