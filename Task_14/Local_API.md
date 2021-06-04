# Load data from local API
- Start our HTTP-Server `bookmonkey-api` in your shell.
- Import the `HttpClientModule` in your `AppModule`.
- Inject `HttpClient` via `constructor(private http: HttpClient)` in `BookApiService`
- Load data from local API in `BookApiService` service via `http.get(URL)`

## Hints

## API starten

```bash
# console session
npm i -g bookmonkey-api
bookmonkey-api
# OR
npx bookmonkey-api
```

```typescript
import { HttpClientModule } from '@angular/common/http';
```

```typescript
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
```

```typescript
return this.http.get<Book[]>('http://localhost:4730/books')
```

```typescript
this.bookDataService.getBooks().subscribe(successFn);
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--load-data-from-local-api)
