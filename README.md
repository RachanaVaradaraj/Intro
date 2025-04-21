#Intro
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { ReviewDiscrepancyComponent } from './review-discrepancy/review-discrepancy.component';
import { MatchStatusComponent } from './match-status/match-status.component';
import { ReportComponent } from './report/report.component';
import { FileUploadComponent } from './file-upload/file-upload.component';

const routes: Routes = [
  { path: '', component: FileUploadComponent },
  { path: 'review-discrepancy', component: ReviewDiscrepancyComponent },
  { path: 'match-status', component: MatchStatusComponent },
  { path: 'report', component: ReportComponent }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule {}