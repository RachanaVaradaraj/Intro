import { Component } from '@angular/core';
import { HttpClient, HttpClientModule } from '@angular/common/http';
import { CommonModule } from '@angular/common';
import { MatButtonModule } from '@angular/material/button';
import { MatIconModule } from '@angular/material/icon';
import { MatListModule } from '@angular/material/list';

@Component({
  selector: 'app-file-upload',
  standalone: true,
  imports: [
    CommonModule,
    HttpClientModule,
    MatButtonModule,
    MatIconModule,
    MatListModule
  ],
  templateUrl: './file-upload.component.html',
  styleUrls: ['./file-upload.component.css']
})
export class FileUploadComponent {
  files: File[] = [];
  isDragOver = false;

  constructor(private http: HttpClient) {}

  onFileSelected(event: any) {
    const selectedFiles = Array.from(event.target.files) as File[];
    this.files.push(...selectedFiles);
  }

  removeFile(index: number) {
    this.files.splice(index, 1);
  }

  uploadFiles() {
    if (this.files.length === 0) return;

    const formData = new FormData();
    this.files.forEach(file => formData.append('files', file));

    this.http.post('http://localhost:8080/upload', formData).subscribe(
      res => {
        alert('Files uploaded successfully!');
        this.files = [];
      },
      err => {
        alert('Upload failed.');
      }
    );
  }

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
}