# React Lab Exercise 10: React Strict Mode
## Name: PREM PRASANTH J
## Roll no: 2305001028
## Department: CSE

## AIM

To implement React Strict Mode and understand how it helps detect potential problems and unexpected side effects during development.

## PROGRAM

### i) main.jsx
```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import "./index.css";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <App />
  </StrictMode>
);
```

### ii) App.jsx
```jsx
import { useEffect, useState } from "react";
import "./App.css";

function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log("Effect started");

    return () => {
      console.log("Effect cleanup");
    };
  }, []);

  return (
    <div className="container">
      <h1>React Strict Mode</h1>
      <h2>Count: {count}</h2>

      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>

      <p>
        React Strict Mode helps detect potential problems
        during development.
      </p>
    </div>
  );
}

export default App;
```

## OUTPUT
<img width="1136" height="464" alt="image" src="https://github.com/user-attachments/assets/2584c0ff-7dca-40cc-b01a-4020267bd522" />

## RESULT

Thus, React Strict Mode was successfully implemented in a React application. The counter was tested, and the effect setup and cleanup behavior was observed during development.
