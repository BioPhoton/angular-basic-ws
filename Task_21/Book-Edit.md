# Create a BookEdit Component
1. Create a new Component with ng-cli
2. Add a link from `BookDetail` to `BookEdit` (use `routerLink`)
3. Extend the `Routes`
4. Add `FormsModule` to imports of `BookModule` (@angular/forms) 
5. Create simple form and inspect the componentInstance

## Hints

**Generate BookEdit component**

```bash
ng generate component books/book-edit
```

**RouterLink in BookDetail**
```html
<a [routerLink]="['edit']">Edit</a>
```

**BookEdit Form**
```html
<form #form="ngForm">
  <input
    type="text"
    [(ngModel)]="book.title" 
    name="title"
    #title="ngModel">
</form>
```

Analyse form via: `ng.probe($0)`
