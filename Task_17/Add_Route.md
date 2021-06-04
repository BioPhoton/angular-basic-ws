# Add basic routing
1. Import your BookListComponent to your books-routing module
2. Add a route for your BookListComponent
3. Import your AboutComponent to your about-routing module
4. Add a route for your AboutComponent
5. Add a default route for the root path which redirects to ‘/books’ in app-routing.module.ts
6. Add routerLinks to NavigationComponent

Don’t forget to remove book-list from your app components template, otherwise you will see it twice :-)

## Hints

#### Book Routes:

```
const routes: Routes = [
{
  path: '',
  pathMatch: 'full',
  redirectTo: '/about'
},
{
  path: 'about',
  component: AboutComponent
}]
```

#### Router outlet:

`<router-outlet></router-outlet>`
