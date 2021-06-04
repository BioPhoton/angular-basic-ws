# Generate two Submodules

1. Generate 2 sub Modules with a routing (we will learn later more about it)
    - about
    - books
    
2. Generate for each of these modules a root-component named like the module
3. use BooksComponent in app.component.html and check the devTools
4. BooksModule needs to export BooksComponent
5. AppModule needs to import BooksModule

Protip: Use the CLI Generator for this (--routing and -m)

## Hints

#### generate a whole module as submodule
```
ng g module books --routing -m app.module
ng g module about --routing -m app.module
```

####  generate a root-component in a subfolder for a module
```
ng g c books/books --export
ng g c about/about --export
```
#### app.component.html
```
<books></books>
<router-outlet></router-outlet>
```
#### books.module.ts
```
@NgModule({
  imports: [
    CommonModule,
    BooksRoutingModule
  ],
  exports: [BooksComponent],
  declarations: [BooksComponent]
})
export class BooksModule { }
```
