# Extend the BookEdit Component
1. Extend the BookEdit form with inputs for `title`, `abstract` and `author`
2. Add validations to your inputs
3. Create error messages for your validations
4. Create a basic `save` function with console.log
5. Add validation CSS styles for the component

## Hints

required, minlength

```html
<div [hidden]="!title.errors?.required || title.pristine">…</div>
```

```html
<form #form="ngForm" (ngSubmit)="save(form.value)">…</form>
```

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Extend-the-BookEdit-Component)
