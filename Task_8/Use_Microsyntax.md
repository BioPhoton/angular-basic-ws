# Use Microsyntax
We already have a component being capable of rendering a book.
Let's instrument the component to render a whole list.

- Open _src/app/app.component.ts_.
- Rename the property _book_ to _books_.
- Change the type of `books` from `Book` to `Book[]` .
- Wrap your book with a list.
- Add at least one additional book to your list.
- Switch to the template of _AppComponent_.
- Add the attribute `*ngFor` to `<app-book-card>` to render all books of your list.
- Have a look at the browser to check the result.

## Hints

```ts
// app.component.ts
books: Book[] = [
  {
    title: 'How to win friends',
    author: 'Dale Carnegie',
    abstract: "How to Win Friends and Influence ..."
  },
  {
    title: 'The Willpower Instinct: How Self-Control Works ...',
    author: 'Kelly McGonigal',
    abstract: 'Based on Stanford University ...'
  },
  {
    author: 'Simon Sinek',
    title: 'Start with WHY',
    abstract: "START WITH WHY shows that the leaders who've ..."
  }
];
```

```html
<!-- app.component.html -->
<app-book-card ... *ngFor="let book of books">
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--use-structure-syntax)
