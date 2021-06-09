# Material Component Harness (Forms)
- Create _book-new.component.spec.ts_ next to book-new.component.ts, if the file not exists.
- Write a tests ensuring that an error hint is shown if the typed ISBN has less than 3 characters.
- Use `MatFormFieldHarness` & `MatInputFieldHarness` to implement the test.
- _Note, the error message of a MatInputField is shown after the user leaves (blur) the input._

## Hints

```ts
beforeEach(() => {
  TestBed.configureTestingModule({
    declarations: [BookNewComponent],
    imports: [
      NoopAnimationsModule, // Is needed since @angular/material deals with animations
      // <INSERT MISSING IMPORTS TO GET THE MODULE RUNNING>
    ]
  });

  fixture = TestBed.createComponent(BookNewComponent);
  loader = TestbedHarnessEnvironment.loader(fixture);

  fixture.detectChanges();
})



```
