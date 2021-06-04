# Create an observable
1. The `getBooks()` method should use `of()`
2. Subscribe to it in the BookList component

## Hints

#### imports

`import { Observable, of } from 'rxjs';`

#### getBooks()

`return of(this.books);`

#### Component

`.subscribe(successFn)`

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Create-an-observable)
