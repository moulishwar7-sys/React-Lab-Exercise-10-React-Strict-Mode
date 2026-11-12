# React-Lab-Exercise-10-React-Strict-Mode

## Name : Moulishwar G
## Register Number : 2305001020

# Aim
To implement React Strict Mode and understand how it helps detect potential problems and unexpected side effects during development.

# Program
## main.jsx
```python
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
## App.jsx
```python
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

# Output:

<img width="1136" height="464" alt="702488023-2584c0ff-7dca-40cc-b01a-4020267bd522" src="https://github.com/user-attachments/assets/ed117f2c-a6f8-46ac-ac5f-b8f8564fb2f1" />

# Result:

Thus, React Strict Mode was successfully implemented in a React application. The counter was tested, and the effect setup and cleanup behavior was observed during development.


