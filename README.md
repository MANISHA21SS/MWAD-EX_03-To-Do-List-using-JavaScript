# MWAD-EX_03-To-Do-List-using-JavaScript
## Date: 17/9/2025

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

index.html
```
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="todo-container">
        <h1>My To-Do List</h1>
        <div class="input-section">
            <input type="text" id="taskInput" placeholder="Enter a task">
            <button id="addBtn">Add</button>
        </div>
        <ul id="taskList"></ul>
        <button id="clearBtn">Clear All</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
```
style.css

```
body {
    font-family: Arial, sans-serif;
    background-color:pink;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.todo-container {
    background: rgb(153, 121, 182);
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    width: 300px;
    text-align: center;
}

.input-section {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
}

#taskInput {
    flex: 1;
    padding: 5px;
}

button {
    padding: 5px 10px;
    cursor: pointer;
}

li {
    display: flex;
    justify-content: space-between;
    padding: 5px;
    border-bottom: 1px solid #eee;
}

li.completed span {
    text-decoration: line-through;
    color: gray;
}
```
script.js
```
const taskInput = document.getElementById("taskInput");
const addBtn = document.getElementById("addBtn");
const taskList = document.getElementById("taskList");
const clearBtn = document.getElementById("clearBtn");

addBtn.addEventListener("click", () => {
    const taskText = taskInput.value.trim();
    if(taskText !== "") {
        const li = document.createElement("li");
        li.innerHTML = `
            <span>${taskText}</span>
            <div>
                <button class="completeBtn">✔</button>
                <button class="deleteBtn">✖</button>
            </div>
        `;
        taskList.appendChild(li);
        taskInput.value = "";

        li.querySelector(".completeBtn").addEventListener("click", () => {
            li.classList.toggle("completed");
        });

        li.querySelector(".deleteBtn").addEventListener("click", () => {
            li.remove();
        });
    }
});


clearBtn.addEventListener("click", () => {
    taskList.innerHTML = "";
});
```


## OUTPUT

<img width="1889" height="901" alt="Screenshot 2025-09-17 084531" src="https://github.com/user-attachments/assets/ca00237b-2dc6-41b9-9cdf-9d85277daca2" />
<img width="1920" height="1080" alt="Screenshot (319)" src="https://github.com/user-attachments/assets/bf6df035-150f-4488-a9e7-e9e07367975b" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
