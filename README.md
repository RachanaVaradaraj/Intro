import { Component, OnInit } from '@angular/core';
import { HttpClient } from '@angular/common/http';

@Component({
  selector: 'app-match-status',
  templateUrl: './match-status.component.html',
  styleUrls: ['./match-status.component.css']
})
export class MatchStatusComponent implements OnInit {
  matchMessage: string = '';

  constructor(private http: HttpClient) {}

  ngOnInit(): void {
    this.http.get('http://localhost:8081/api/match-status', { responseType: 'text' })
      .subscribe({
        next: (data) => this.matchMessage = data,
        error: (error) => console.error('Error fetching match status:', error)
      });
  }
}