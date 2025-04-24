isDragOver = false;

onDragOver(event: DragEvent) {
  event.preventDefault();
  this.isDragOver = true;
}

onDragLeave(event: DragEvent) {
  event.preventDefault();
  this.isDragOver = false;
}

onDrop(event: DragEvent) {
  event.preventDefault();
  this.isDragOver = false;
  if (event.dataTransfer && event.dataTransfer.files.length > 0) {
    const droppedFiles = Array.from(event.dataTransfer.files);
    this.files.push(...droppedFiles);
  }
}