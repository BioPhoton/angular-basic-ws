- Add a new Module `AppRoutingModule` (if you haven't already.)
    - This time, we need to do it manually, by creating a file (app-routing.module.ts) and setting up the code on our own.
- Add Angular's `RouterModule` to the `imports`- & `exports`-Collection.
- Add a constant `routes`.
- Pass `routes` to the `RouterModule`'s `forRoot` function.
- Configure the start route, redirecting to `/books`.
- Configure a book route, displaying the `BookComponent` (path: _books_).
- Switch to _AppModule_.
- Add the `AppRoutingModule` to the `imports`- Collection.
- Switch to _app.component.html_.
- Replace its content with `router-outlet`.
- Use the directive `routerLink` for the 2 links to navigate between the views.
## Hints

#### App Routes:

```
const routes: Routes = [
{
  path: '',
  pathMatch: 'full',
  redirectTo: '/about'
}]
```

#### Book Routes:

```
const routes: Routes = [
{
  path: 'books',
  component: BookComponent
}]
```

#### About Routes:

```
const routes: Routes = [
{
  path: 'about',
  component: AboutComponent
}]
```

#### Router outlet:

`<router-outlet></router-outlet>`

[Solution](https://stackblitz.com/edit/github-gwxssc?file=src/app/app.component.html)
