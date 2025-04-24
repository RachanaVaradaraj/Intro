.upload-container {
  max-width: 600px;
  margin: 50px auto;
  text-align: center;
  padding: 30px;
  border-radius: 10px;
  background-color: #f5f5f5;
  transition: background-color 0.3s, border 0.3s;
}

.upload-container.drag-over {
  background-color: #e0f7fa;
  border: 2px dashed #00796b;
}

.file-label {
  display: inline-block;
  padding: 30px;
  border: 2px dashed #3f51b5;
  border-radius: 8px;
  color: #3f51b5;
  cursor: pointer;
  transition: background-color 0.3s;
}

.file-label:hover {
  background-color: #e3f2fd;
}

.file-list {
  margin-top: 20px;
  text-align: left;
}