# Build a simple canDeactivate guard
1. Create a guard service
2. Open a confirm box
3. Return the confirm value
4. use it for your `BooksDetail` route
## Hints

## Preparation

```
ng generate guard books/confirm-candeactivate
```

## Guard service:
- import CanDeactivate hook from @angular/router
- add interface to your class
- implement canDeactivate() function

```js
return confirm('Are you sure?');
```


Add guard to route:

```ts
{
  path: ...,
  component: ...,
  canDeactivate: [...]
}
```

```ts
implements CanDeactivate<???>
```
