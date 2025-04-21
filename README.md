import { Routes } from '@angular/router';
import { FileUploadComponent } from './file-upload/file-upload.component';
import { ReviewDiscrepancyComponent } from './review-discrepancy/review-discrepancy.component';
import { MatchStatusComponent } from './match-status/match-status.component';
import { ReportComponent } from './report/report.component';

export const routes: Routes = [
  { path: '', component: FileUploadComponent },
  { path: 'review-discrepancy', component: ReviewDiscrepancyComponent },
  { path: 'match-status', component: MatchStatusComponent },
  { path: 'report', component: ReportComponent }
];