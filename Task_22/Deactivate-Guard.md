# Build a simple canDeactivate guard
- Create a guard service: `ng generate guard confirm-leave`.
- Use `window.confirm` to ask the user if he really want to leave the page.
- Open _BookRoutingModule_
- Add the guard to the route `:isbn`

## Hints

## Guard service

- Import CanDeactivate hook from @angular/router
- Add interface to your guard service
- Implement canDeactivate() function

```ts
return confirm('Do you really want to leave?');
```


Add guard to route:

```ts
{
  path: ...,
  component: ...,
  canDeactivate: [...]
}
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--build-a-can-deactivate-guard)
