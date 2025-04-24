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

