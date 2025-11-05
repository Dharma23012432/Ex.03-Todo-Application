# Ex03 To-Do List using JavaScript

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
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Todo App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    .container {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 5px rgba(0,0,0,0.1);
      width: 300px;
      margin: auto;
    }
    input {
      width: 70%;
      padding: 8px;
    }
    button {
      padding: 8px;
      margin: 5px;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      background: #f0f0f0;
      margin: 5px 0;
      padding: 8px;
      border-radius: 5px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .completed {
      text-decoration: line-through;
      color: gray;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Todo App</h2>
    <input type="text" id="taskInput" placeholder="Add a task">
    <button onclick="addTask()">Add</button>
    <ul id="taskList"></ul>
  </div>

  <script>
    const taskInput = document.getElementById('taskInput');
    const taskList = document.getElementById('taskList');

    function addTask() {
      const taskText = taskInput.value.trim();
      if (taskText === '') return;

      const li = document.createElement('li');
      li.textContent = taskText;

      li.addEventListener('click', () => {
        li.classList.toggle('completed');
      });

      const deleteBtn = document.createElement('button');
      deleteBtn.textContent = 'X';
      deleteBtn.onclick = () => li.remove();

      li.appendChild(deleteBtn);
      taskList.appendChild(li);

      taskInput.value = '';
    }
  </script>
</body>
</html>

```

## OUTPUT
<img width="1919" height="1030" alt="image" src="https://github.com/user-attachments/assets/51437219-9f0d-47c0-8264-d44a65a4af3b" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
