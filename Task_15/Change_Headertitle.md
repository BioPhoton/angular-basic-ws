# Change Header title on BookListItem-Click

1. Refactor Expose your Subject as an Observable to your HeaderComponent
2. Implement a `(click)`-Handler inside your `BookListItem`-Component, which calls the `setHeader`-function of the `HeaderService`
3. Change the `setHeader`-function accordingly (the subject should emit now the incoming Headertitle and not a static string anymore)
4. Don't forget to use the async pipe inside the `HeaderComponent` to subscribe to the `headerTitle$`-Observable

## Hints

```
setHeader(headerTitle: string) {
	this.headerService.setHeader(headerTitle)
}
```

```
<h1>{{ headerTitle$ | async }}</h1>
