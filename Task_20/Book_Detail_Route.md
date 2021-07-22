# Add BookDetail Route
Now we get to know more about our books.
The API delivers additional information like ISBN, Cover-Image etc.
It is time to spend a Details-View to our book application.

- Open the _Book_-Interface.
- Add at least two properties to show more information of the book.
    - isbn: string; (mandatory)
    - cover: string;
    - numPages: number;
    - subtitle: string;
    - publisher: { name: string, url: string };
- Create a new Component `BookDetail` with the Angular CLI: `ng generate component book/book-detail`.
- Open _AppRoutingModule_.
- Add the route for the details view: _books/:isbn_.
- Use the routerLink Direktive in the BookCard HTML Template, to navigate the details view.
- Open _BookApiService_.
- Extend the _BookApiService_ allowing to load a book with its ISBN (`getBookByIsbn(isbn: string)`).
- Open _BookDetailComponent_.
- Inject both `ActivatedRoute` & `BookApiService`
- Extract the ISBN from the route-`params`.
- Use `BookApiService` to load the book.
- Setup a template displaying the book information.
    - You can reuse some parts of the BookCardComponent's template, if you like.
## Hints

**Implement the Component**

```typescript
// book-detail.component

import { ActivatedRoute } from '@angular/router';

constructor(private route: ActivatedRoute, private bookApi: BookApiService) { }
```

```typescript
ngOnInit () {
  this.route.params.subscribe((params) => { ... });
}
```

**Extend BookCard HTML with routerlink**

```html
// book-card.component.html

<h3>{{ content.title }}</h3>
<h4>{{ content.author }}</h4>
<a [routerLink]="['/books', content.isbn ]">Details</a>
<p>
    {{ content.abstract }}
</p>
```


**Extend your Routing Module**

```ts
// app-routing.module.ts

{ path: 'book/:isbn', component: BookDetailComponent }
```

**Extend and use the Service with a getBookByIsbn(isbn: string)**
```
HTTP GET http://localhost:4730/books/:isbn
```


[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--add-BookDetail-route)
