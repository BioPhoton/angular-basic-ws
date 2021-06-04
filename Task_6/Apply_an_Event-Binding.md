# Apply an Event-Binding
- Open _src/app/book-card/book-card.component.html_
- Bind to the event `click` of the `<a>`-Tag (aka. Detailslink).
- Assign the method `handleDetailClick($event)` to the Event-Binding.
- Switch to the component class.
- Implement the new method `handleDetailClick(click: MouseEvent)`.
- Log the value of the parameter `handleDetailClick` to the console.
- Prevent the page to reload by preventing the default behaviour of the link's click event _(see hint)_.
- Ensure your implementation works by checking your app at [localhost:4200](http://localhost:4200).
- Open the browser's console to see the log messages.

## Hints

```ts
detailClick(click: MouseEvent) {
  click.preventDefault();
  
  console.log('Click Details-Link': click)
}
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--apply-an-event-binding)
