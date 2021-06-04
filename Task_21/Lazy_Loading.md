# Use Lazy Loading for BooksModule
- Open _AppModule_.
- Remove BooksModule from `imports`-Collection.
- Create a new module _BookRoutingModule_ configuring child routes.
- Open _AppRoutingModule_.
- Transfer the routes _books/detail_ & _books_ to _BookRoutingModule_.
    - Pay attention to the hints: The paths will slightly change.
- Add a lazy loaded route for the path `books` loading the _BookModule_.
- Open your app in the browser
- Open the Developer Tools
- Open the Network Tab
- Make sure that _book-book-module.js_ appears in the list of network requests.

> *Sometimes the introduction of a lazy loaded module causes problems with the Angular CLI. The app still works after the change but you do not see that BookModule is loaded lazyly. A restart `ng serve` will help.*
## Hints

```ts
// app-routing.module.ts
const routes: Routes = [
  {
    path: '',
    pathMatch: 'full',
    redirectTo: '/about'
  },
  {
    path: 'books',
    loadChildren: () =>
      import('./book/book.module').then(module => module.BookModule)
  },
  {
    path: 'about',
    component: AboutComponent
  }
];
```

```ts
// books-routing.module.ts

const routes: Routes = [
  {
    path: '',
    component: BookComponent
  },
  {
    path: 'details/:isbn',
    component: BookDetailComponent
  }
];

// ...
RouterModule.forChild(routes)
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--use-lazy-loading-for-BookModule)
