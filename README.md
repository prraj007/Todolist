# Ex03 To-Do List using JavaScript
## Date:

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

todo.jsx

```
import { useState, useRef } from "react";
import "./todo.css";

function ToDo() {
  const [tasks, setTasks] = useState([]);
  const name = useRef();
  const desc = useRef();
  const kind = useRef();
  const date = useRef();
  const time = useRef();

  function addTask() {
    const task = {
      name: name.current.value,
      desc: desc.current.value,
      kind: kind.current.value,
      date: date.current.value,
      time: time.current.value
    };

    setTasks([...tasks, task]);
  }

  return (
    <>
      <h1>My Todo List</h1>

      <div className="box">
        <input ref={name} placeholder="Enter task" />
        <textarea ref={desc} placeholder="Enter description" />

        <select ref={kind}>
          <option>Personal</option>
          <option>College</option>
          <option>Shopping</option>
          <option>Workout</option>
        </select>

        <input type="date" ref={date} />
        <input type="time" ref={time} />

        <button onClick={addTask}>Add</button>
      </div>

      <div className="tasks">
        {tasks.map((task, i) => (
          <div className="task" key={i}>
            <b>{task.name}</b>
            <p>{task.desc}</p>
            <p>{task.kind}</p>
            <small>{task.date} | {task.time}</small>
          </div>
        ))}
      </div>
    </>
  );
}

export default ToDo;
```

css

```
* {
  box-sizing: border-box;
  font-family: Arial;
}

body {
  margin: 0;
  background: #f4f7fb;
}

h1 {
  margin: 0;
  padding: 25px;
  text-align: center;
  color: white;
  background: linear-gradient(135deg, #2563eb, #06b6d4);
}

.box, .task {
  width: 90%;
  max-width: 700px;
  margin: 25px auto;
  padding: 20px;
  background: white;
  border-radius: 10px;
  box-shadow: 0 5px 15px #ccc;
}

input, textarea, select {
  width: 100%;
  padding: 12px;
  margin: 7px 0;
  border: 1px solid #ccc;
  border-radius: 6px;
}

textarea {
  height: 80px;
}

button {
  padding: 10px 30px;
  background: #2563eb;
  color: white;
  border: 0;
  border-radius: 6px;
  cursor: pointer;
}

.task {
  margin: 15px auto;
}

.task b {
  font-size: 20px;
}

.task p {
  margin: 8px 0;
}
```


## OUTPUT
<img width="1917" height="1075" alt="image" src="https://github.com/user-attachments/assets/4b64b5cf-ab7e-4dec-9d32-2dba03d5f4cc" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
