# Add a BookNew Form and Route
1. Create a new Component with ng-cli, and a route
2. Add a link from `BookList` with `routerLink` to `BookNew`
3. Use __Model-Driven__ form syntax → add `ReactiveFormsModule` to `BooksModule`
4. Extend the `Routes` (Pay attention to the order of the routes!)

## Hints

```sh
ng g c books/book-new
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


[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Add-a-BookNew-Route)
