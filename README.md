.upload-container {
  max-width: 500px;
  margin: 60px auto;
  padding: 30px;
  border-radius: 12px;
  background: #f9f9f9;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.upload-container h2 {
  margin-bottom: 20px;
  color: #333;
}

.upload-box {
  border: 2px dashed #3f51b5;
  padding: 40px 20px;
  border-radius: 10px;
  transition: background-color 0.3s;
  cursor: pointer;
}

.upload-box.dragging {
  background-color: #e3f2fd;
}

.select-btn {
  margin-bottom: 15px;
  padding: 10px 20px;
  background-color: #3f51b5;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}

.select-btn:hover {
  background-color: #303f9f;
}

.error {
  color: red;
  margin-top: 10px;
  font-weight: 500;
}

.preview {
  margin-top: 20px;
  max-width: 100%;
  max-height: 200px;
  border-radius: 6px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}