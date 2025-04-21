#Intro 
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class MatchStatusService {
  private apiUrl = 'http://localhost:8080/api/match-status';

  constructor(private http: HttpClient) {}

  getStatus(): Observable<string> {
    return this.http.get(this.apiUrl, { responseType: 'text' });
  }
}