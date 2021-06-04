# Apply an Input Binding
Now, it is time to feed our component with data using an `@Input`-Binding.

- Open `src/app/book-card/book-card.component.ts`.
- Add a property `content`.
- Annotate the property `content` with `@Input`.
- Switch to the template of _BookCardComponent_ component.
- Bind the values coming with `content` using binding expression (e.g.`{{ content.title }}`).
- Switch to the `src/app/book-card/app.component.ts`.
- Initialize a property `book` with the properties _title_, _author_, _abstract_.
- Switch to the template of _AppComponent_.
- Bind the property `book` to the component `book-card` using its `@Input`-binding **[content]**.

## Hints

```ts
// app.component.ts
export class AppComponent {
  book = {
    title: 'How to win friends',
    author: 'Dale Carnegie',
    abstract: 'In this book ...'
  };
}
```

```html
<!-- bookd-card.component.html -->
<h3>{{ content.title }}</h3>
<!-- ... -->
```



[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--apply-an-input-binding)
