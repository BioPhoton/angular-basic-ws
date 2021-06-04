# Use the async pipe
- Store the `getAll()`-Observable in a class property
- Use the Observable and async pipe to subscribe and unsubscribe inside your `*ngFor`
- **Warning**: This change affects the typing in the template
    - async returns either `Book[]` or `null`
    - You may need to adjust BookFilterPipe to deail with `null`-Values.

## Hints

```typescript
// book-list.component.ts
this.books$ = this.bookData.getAll();
```

```html
<!-- book-list.component.html -->
*ngFor="let book of books$ | async | ..."
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--use-the-async-pipe)
