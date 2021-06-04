# Use the async pipe
1. Store `getBooks()`-Observable on a class property
2. Use the observable and async pipe for subscribe and unsubscribe in your `*ngFor`

## Hints

#### book-list.component.ts

`this.books$ = this.bookData.getBooks();`

#### book-list.component.html

`*ngFor="let book of books$ | async"`
