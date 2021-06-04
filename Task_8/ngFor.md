# Use *ngFor
1. Create a `BookList` component with ng(-cli)
2. Use the new component in the `AppComponent` view
3. Create an array with sample books in your `BookList` component
4. Iterate over books with `*ngFor`

## Hints

`ng generate component books/book-list --export`

`*ngFor="let book of books"`

```
…
books = [
  {
    "title": "Design Patterns",
    "subtitle": "Elements of Reusable Object-Oriented Software"
  },
  {
    "title": "REST und HTTP",
    "subtitle": "Entwicklung und Integration nach dem Architekturstil des Web"
  },
  {
    "title": "Eloquent JavaScript",
    "subtitle": "A Modern Introduction to Programming"
  }
]
…
```

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Use-ngFor)
