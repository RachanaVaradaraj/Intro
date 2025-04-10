# Intro
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 300px;
    text-align: center;
}

h2 {
    color: #333;
    margin-bottom: 20px;
}

.input-container {
    display: flex;
    gap: 10px;
}

input[type="text"] {
    flex: 1;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    background: #28a745;
    color: white;
    border: none;
    padding: 8px 12px;
    cursor: pointer;
    border-radius: 4px;
}

button:hover {
    background: #218838;
}

ul {
    list-style-type: none;
    padding: 0;
    margin-top: 10px;
}

ul li {
    background: #eee;
    padding: 10px;
    margin: 5px 0;
    display: flex;
    justify-content: space-between;
    border-radius: 4px;
}

.delete-btn {
    background: #dc3545;
    color: white;
    border: none;
    padding: 5px;
    cursor: pointer;
    border-radius: 4px;
}

.delete-btn:hover {
    background: #c82333;
}
