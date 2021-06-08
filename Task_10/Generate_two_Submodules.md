# Generate two Submodules

- Generate 2 sub Modules with a routing (we will learn later more about it)
    - about
    - books

- Move all book related code to the `books/`-folder.
    - _book.ts_
    - _book-card/_
    - _book-filter/_
- Create a component that will take all the code of _AppComponent_: `ng generate component books/book`.    
- Open _app.module.ts_.
- Remove all book related code.
    - Remove _BookCardComponent_ & _BookFilterPipe_ from declarations.
- Add _BookModule_ and _AboutModule_ to the `imports`-Collection.
- Transfer the content of _AppComponent_ to _BookComponent_ (only **inside** the class).
- Transfer the content of _app.component.html_ to _book.component.html_.
- Transfer the content of _app.component.scss_ to _book.component.scss_.
- Check if all `import`-statements are correct.

- Generate a simple dummy Component `AboutComponent` inside `AboutModule`

Protip: Use the CLI Generator for this (--routing and -m)

## Hints

#### generate a whole module as submodule
```
ng g module books --routing -m app.module
ng g module about --routing -m app.module
```

####  generate a root-component in a subfolder for a module
```
ng g c about/about
```
#### app.component.html
```
<app-book></app-book>
```
#### books.module.ts
```
@NgModule({
  declarations: [BookComponent, BookCardComponent, BookFilterPipe],
  imports: [CommonModule],
  exports: [BookComponent]
})
export class BooksModule { }
```


[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--create-a-BookModule)
