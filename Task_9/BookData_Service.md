# Create a BookDataService
1. Generate a `Book` interface for a single book in the folder books
2. Generate a `BookData` service in the `books` folder that uses the `Book` interface
3. Add a method `getBooks()` that returns an array of Books
4. Load the data from the `BookData` service through the DI into `BookList` component

## Hints

#### Generate with ng-cli:

```
ng g interface books/book
ng generate service books/book-data
```
#### Code:
```
export interface Book{
  title: string;
  …
}

// book-list.component.ts
constructor(private bookData: BookDataService){}
```
[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Create-a-BookData-service)
