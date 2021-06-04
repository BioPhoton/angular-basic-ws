# Filter books
Since we add more and more books to our list, a filter is helpful to focus the book you want to know more about.

**The Book filter pipe**
- Create a pipe using the CLI: `ng generate pipe book-filter/book-filter`.
- Recognize that _app.module.ts_ is updated after createing the new pipe.
- Open _src/app/book-filter/book-filter.pipe.ts_.
- Enhance the `transform` method of the pipe to filter books by **title**.
- _BONUS_ type the `transform` method as good as possible
- Switch to _src/app/app.component.html_

**The Book filter control**
- Add an _<input>_-Field acting as search field.
- Handle its `(input)`-Event by binding it to a method called `updateBookSearchTerm($event)`.
- Implement the method `updateBookSearchTerm` in _app.component.ts_.
- Extract the value of the input field from the `InputEvent` and store the search term in a property called `bookSearchTerm`.

**Use the bookFilter-Pipe**
- Open _app.component.html_.
- Enhance the `*ngFor`-expression by using the `bookFilter`-Pipe.
- Pass the value of the _<input>_-Field to the pipe by adding the parameter `bookSearchTerm`

**Check the result**
- Open the browser at [localhost:4200](http://localhost:4200)
- Check if the filter works as exepected

**Bonus**
- Style the filter-control (refer to the solution to get some inspiration)
- Extract the filter control into its own Component.


## Hints

```html
// app.component html

// search input
<input (input)="updateSearchTerm($event)">

// use pipe
<app-book-card *ngFor="let book of books | bookFilter: bookSearchTerm">
```

```ts
// app.component.ts

// store input value in property
updateBookSearchTerm(input: Event) {
  this.bookSearchTerm = (input.target as HTMLInputElement).value;
  //                                  ^ tells the TypeScript-Compiler to treat the target property as HTMLInputElement
}

//book-filter.pipe.ts
books.filter(book =>
    book.title.toLocaleLowerCase().includes(searchTerm.toLocaleLowerCase())
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--filter-books)
