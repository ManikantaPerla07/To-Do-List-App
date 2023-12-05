# To-Do-List-App
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>To-Do List App</title>
</head>
<body>
    <div id="app">
        <h1>To-Do List</h1>
        <input v-model="newTask" @keyup.enter="addTask" placeholder="Add a new task">
        <ul>
            <li v-for="(task, index) in tasks" :key="index">
                {{ task }}
                <button @click="editTask(index)">Edit</button>
                <button @click="deleteTask(index)">Delete</button>
            </li>
        </ul>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
    <script src="script.js"></script>
</body>
</html>
