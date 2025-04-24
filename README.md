.upload-container {
  max-width: 600px;
  margin: 50px auto;
  text-align: center;
  padding: 30px;
  border-radius: 10px;
  background-color: #f5f5f5;
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

<div class="upload-container mat-elevation-z4">
  <h2>Upload Your Files</h2>

  <label class="file-label" for="fileInput">
    <mat-icon>cloud_upload</mat-icon>
    <span>Click or Drag to Upload Files</span>
    <input type="file" id="fileInput" (change)="onFileSelected($event)" multiple hidden />
  </label>

  <div *ngIf="files.length > 0" class="file-list">
    <mat-list>
      <mat-list-item *ngFor="let file of files; let i = index">
        <mat-icon matListIcon>insert_drive_file</mat-icon>
        {{ file.name }} ({{ file.size | number }} bytes)
        <button mat-icon-button color="warn" (click)="removeFile(i)">
          <mat-icon>delete</mat-icon>
        </button>
      </mat-list-item>
    </mat-list>
    <button mat-raised-button color="primary" (click)="uploadFiles()">Upload</button>
  </div>
</div>

.file-label:hover {
  background-color: #e3f2fd;
}

.file-list {
  margin-top: 20px;
}