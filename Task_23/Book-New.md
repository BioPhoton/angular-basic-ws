# Add a BookNew Form and Route
1. Create a new Component with ng-cli, and a route
2. Add a link from `BookComponent` with `routerLink` to `BookNew`
3. Add `ReactiveFormsModule` to `BooksModule`
4. Extend the `Routes` (Pay attention to the order of the routes!)

## Hints

```sh
ng generate component books/book-new
```

```typescript
import {Validators, FormBuilder, FormGroup} from '@angular/forms';
```

```html
<form [formGroup]="form" (ngSubmit)="onSubmit()">

<input type="text" formControlName="title">
```

```typescript
form.get('title').hasError('required')
```

```typescript
this.form = this.fb.group({
  'title': ['', [Validators.required]],
  ...
});
```


[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--add-a-BookNew-form-and-route)
