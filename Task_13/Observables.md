# Create an observable
- Change the API of `getAll` returning `Observable<Book[]>` instead of `Book[]`.
- Make use of the creation operator `of`.
- Consume the Observable in the component.
- Make sure that the books are still rendered.

## Hints

**imports**
```typescript
import { Observable, of } from 'rxjs';
```

**getBooks()**
```typescript
return of(this.books);
```

**Component**
```typescript
.subscribe(booksFromApi => /* assign to books */)
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--create-an-observable)
