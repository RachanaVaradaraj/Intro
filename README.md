import { Component, OnInit } from '@angular/core';
import { CommonModule } from '@angular/common';
import { MatchStatusService } from '../match-status.service';

@Component({
  selector: 'app-match-status',
  standalone: true,
  imports: [CommonModule],
  template: `
    <div class="status-box">
      <h2>Match Status</h2>
      <p>{{ statusMessage }}</p>
    </div>
  `
})
export class MatchStatusComponent implements OnInit {
  statusMessage = '';

  constructor(private matchStatusService: MatchStatusService) {}

  ngOnInit(): void {
    this.matchStatusService.getStatus().subscribe(response => {
      this.statusMessage = response;
    });
  }
}