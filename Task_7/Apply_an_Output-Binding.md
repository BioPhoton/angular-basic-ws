# Apply an Output-Binding
It is time to allow our component to communicate with other components.

- Open _src/app/book-card/book-card.component.ts_
- Initialize a property `detailClick` with an `EventEmitter`.
- Type the `EventEmitter` to accept a `Book` as event payload.
- Annotate `detailClick` with the `@Output` decorator.
    - Make sure `@Output` & `EventEmitter` are imported from `@angular/core`.
- Emit the `detailClick`-Event within `handleDetailClick`.
- Switch to _src/app/app.component.html_
- Bind to the `detailClick`-Event of _<app-book-card>_ to a method `goToBookDetails($event)`
- Implement `goToBookDetails($event)` by logging book passed by _<app-book-card>_

## Hints

```ts
// src/app/book-card/book-card.component.ts

// Output-Binding
@Output() detailClick = new EventEmitter<Book>();

// Emit an event
this.detailClick.emit(this.content);
```

```ts
// src/app/app.component.ts

// handling detailClick-Event
goToBookDetails(book: Book) {
  console.log('Navigate to book details, soon...');
  console.table(book);
}
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--apply-an-output-binding)
