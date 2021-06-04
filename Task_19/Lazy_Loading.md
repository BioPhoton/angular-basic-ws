# Use Lazy Loading for BooksModule
1. Remove BooksModule from `imports` in AppModule
2. Add books route to `app-routing.module.ts`
3. Set base books path to `''`
4. Restart your `ng serve` since it has new starting points to compile
5. Make sure your `BooksComponent`-View holds a `<router-outlet></router-outlet>`

## Hints

```
// app-routing.module.ts
const routes: Routes = [
  {path: '', redirectTo: '/about', pathMatch: 'full'},
  {path: 'books', loadChildren: () => import('./books/books.module').then(m => m.BooksModule)}
];
```

```
// books-routing.module.ts
const routes: Routes = [{
  path: '',
  component: BooksComponent,
}, ...];
```
