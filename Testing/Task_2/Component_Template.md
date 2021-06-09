# Component Template
- Write a test ensuring that the bound `Input`-Property is rendered in the template.
- Place the test in _book-card.component.spec.ts_.
- Setup `TestBed` to create a fixture for _BookCardComponent_.
- Make sure that `TestBed` configures all dependencies (declarations, imports) of _BookCardComponent_.
- Use `fixture.detectChanges()` for rendering component properties to the template.
- Use `fixture.debugElement.query()` to access an Element in the template.
- Assert that the element contains the respective `content`-value.
## Hints

```ts
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { By } from '@angular/platform-browser';

TestBed.configureTestingModule({
  declarations: [BookCardComponent],
  imports: [/* ... */]
});

let fixture: ComponentFixture<BookCardComponent>;
fixture = TestBed.createComponent(BookCardComponent);
fixture.detectChanges();
```
