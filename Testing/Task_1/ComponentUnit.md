# Component Unit
- Create _book-card.component.spec.ts_ next to book-card.component.ts, if the file not exists.
- Test the class `BookCardComponent` without its template.
- Assert that after initializing the class all properties of `content` default to `"n/a"`.

## Hints

```ts
describe('<app-book-card>', () => {
  describe('When no content is passed', () => {
    it('defaults to "n/a"', () => {
       // Write your test here, please
    });
  })
})
```
