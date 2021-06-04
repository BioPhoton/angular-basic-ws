# Make an Input-Binding typesafe
We can embrace TypeScripts language features to make developing with Angular more comfortable.

- Create an _Interface_ called `Book`.
- Execute following command to create the interface: `ng generate interface book`.
- Open _src/app/book.ts_.
- Specify the following properties: _title_, _abstract_, _author_.
- Switch to the _AppComponent_.
- Annotate the property book with the interface `Book`.
    - You might need to import `Book` from _'./book'_ if your editor misses to import the type automatically.
- Switch to the _BookCardComponent_.
- Annotate the @Input-property content with the interface `Book`.
- Recognize that you now have auto-completion in both TypeScript- & Template-Files.
## Hints

```ts
// app.component.ts
book: Book = { /* ... */ };

// book-card.component.ts
@Input() content: Book;
```


[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--maken-an-input-binding-typesafe)
