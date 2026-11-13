# Exp 5 – React Lab Exercise: Form Handling in React

## NAME : Mahesh N
## REG NO : 2305001017

## Aim
To develop a simple Student Registration Form using React and handle form input values using the `useState` Hook.

## Objectives
- To create a form using React.
- To create input fields such as Name, Register Number, and Department.
- To use `useState()` to store form data.
- To handle input changes using `onChange`.
- To handle form submission using `onSubmit`.
- To display submitted student details.

## Program

### Step 1 – Create React Project

```bash
npm create vite@latest react-form
cd react-form
npm install
npm run dev
```

Select React as the framework and JavaScript as the variant.

### Step 2 – App.jsx

```jsx
import { useState } from "react";
import "./App.css";

function App() {
  const [name, setName] = useState("");
  const [registerNo, setRegisterNo] = useState("");
  const [department, setDepartment] = useState("");

  const handleSubmit = (event) => {
    event.preventDefault();

    alert(
      "Name: " + name +
      "\nRegister Number: " + registerNo +
      "\nDepartment: " + department
    );
  };

  return (
    <div className="container">
      <h1>Student Registration Form</h1>

      <form onSubmit={handleSubmit}>
        <label>Name:</label>
        <input
          type="text"
          value={name}
          onChange={(event) => setName(event.target.value)}
          placeholder="Enter your name"
          required
        />

        <label>Register Number:</label>
        <input
          type="text"
          value={registerNo}
          onChange={(event) => setRegisterNo(event.target.value)}
          placeholder="Enter register number"
          required
        />

        <label>Department:</label>
        <input
          type="text"
          value={department}
          onChange={(event) => setDepartment(event.target.value)}
          placeholder="Enter department"
          required
        />

        <button type="submit">Submit</button>
      </form>
    </div>
  );
}

export default App;
```

### Step 3 – App.css

```css
.container {
  width: 400px;
  margin: 50px auto;
  padding: 25px;
  border: 1px solid gray;
  border-radius: 10px;
}

h1 {
  text-align: center;
  color: blue;
}

label {
  display: block;
  margin-top: 15px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  box-sizing: border-box;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
```

## Output

### Entered Student Details
<img width="945" height="897" alt="WhatsApp Image 2026-11-02 at 7 40 57 PM" src="https://github.com/user-attachments/assets/d72535f6-af86-4778-bd85-ac0cc46e1645" />

### Submitted Details – Alert Box
<img width="950" height="892" alt="WhatsApp Image 2026-11-02 at 7 43 18 PM" src="https://github.com/user-attachments/assets/01ee3471-46a5-4971-9a7b-4e212ff39d99" />

## Result

Thus, a Student Registration Form was successfully created using React. Form input values were managed using the `useState()` Hook, input changes were handled using `onChange`, and form submission was handled using `onSubmit`. The submitted student details were successfully displayed using an alert box.
