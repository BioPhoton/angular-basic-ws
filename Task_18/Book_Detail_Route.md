# Add BookDetail Route
1. Create a new Component BookDetail with angular-cli
2. Extend BookList with routerLink to create URL with ISBN parameter
3. Extend the Routes with a BookDetail route
4. Extend BookData service with getBookByIsbn(isbn: string)
5. Load data from service via getBookByIsbn(isbn: string) into BookDetail
6. Extend the BookDetail Template to display all data of a specific book in the view

## Hints

#### Generate the Component

ng generate component books/book-detail
#### Implement the Component
BookDetailComponent

```
import {ActivatedRoute} from '@angular/router';

constructor(private route: ActivatedRoute) { }
```
```
ngOnInit () {
  this.route.params.subscribe((params: {isbn: string}) => { ... });
}
```

#### Extend BookList HTML with routerlink
absolute

`<a [routerLink]="['/books', book.isbn]">...</a>`
relative

`<a [routerLink]="[book.isbn]">...</a>`
#### Extend your Routing Module
Routes

`{ path: 'books/:isbn', component: BookDetailComponent }`
#### Extend and use the Service with a getBookByIsbn(isbn: string)

`HTTP GET http://localhost:4730/books/:isbn`

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Add-BookDetail-Route)
