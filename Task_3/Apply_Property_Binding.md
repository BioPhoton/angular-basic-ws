# Apply a property binding
Let's smoothly start with Angular's binding capabilities.

- Open _src/app/book-card/book-card.component.ts_.
- Initialize a property `customStyle` with an object containing css-Styles _(see Hint for more information)_.
- Switch to the template of the component.
- Add a property binding to one HTML-Element of you choice.
    - Use a `[style]`-Binding.
    - Assign `customStyle` as value of the binding expression.


## Hints

```ts
export class BookCardComponent {
  customStyle = {
    color: 'red'
  };
}
```

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--apply-a-property-binding)
