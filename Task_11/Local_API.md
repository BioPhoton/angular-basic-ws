# Load data from local API
1. Start our HTTP-Server bookmonkey-api in your shell
2. Import the HttpClientModule in your AppModule.
3. Inject HttpClient via constructor(private http: HttpClient) in BookData
4. Load data from local API in BookData service via http.get(URL)

## Hints

`import {HttpClientModule} from "@angular/common/http";`

```
import {HttpClient} from '@angular/common/http';
import {Observable} from 'rxjs';
```

`return this.http.get<Book[]>('http://localhost:4730/books')`

`this.bookDataService.getBooks().subscribe(successFn);`

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Load-data-from-local-API)
