import { Component, OnInit } from '@angular/core';
import { MatchStatusService } from '../match-status.service';

@Component({
  selector: 'app-match-status',
  templateUrl: './match-status.component.html'
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