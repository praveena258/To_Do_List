# Ex03 To-Do List using JavaScript
## Date:12.05.26

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
html code
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>To-Do List</h1>
        <div class="input-section">
            <input type="text" id="taskInput" placeholder="Enter a task">
            <button onclick="addTask()">Add</button>
        </div>
        <ul id="taskList"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>
```
css code
```
body {
    font-family: Arial, sans-serif;
    background: #f4f4f4;
    display: flex;
    justify-content: center;
    margin-top: 50px;
}

.container {
    background: white;
    padding: 20px;
    border-radius: 10px;
    width: 350px;
    box-shadow: 0 0 10px gray;
}

.input-section {
    display: flex;
    gap: 10px;
}

input {
    flex: 1;
    padding: 10px;
}

button {
    padding: 10px;
    background: blue;
    color: white;
    border: none;
    cursor: pointer;
}

li {
    list-style: none;
    padding: 10px;
    margin-top: 10px;
    background: #eee;
    display: flex;
    justify-content: space-between;
}

.completed {
    text-decoration: line-through;
    color: gray;
}
```
js code 
```
function addTask() {
    let taskInput = document.getElementById("taskInput");
    let taskText = taskInput.value;

    if (taskText === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");
    li.textContent = taskText;

    li.onclick = function () {
        li.classList.toggle("completed");
    };

    let deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";

    deleteBtn.onclick = function () {
        li.remove();
    };

    li.appendChild(deleteBtn);
    document.getElementById("taskList").appendChild(li);

    taskInput.value = "";
}
```
## OUTPUT
<img width="1907" height="968" alt="image" src="https://github.com/user-attachments/assets/9b069ebb-9888-4ef3-be8f-57dfcbf517b5" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
