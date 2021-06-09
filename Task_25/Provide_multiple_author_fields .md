# Provide multiple author fields

1. Change the `author` FormControl to a `FormArray`
2. Create a getter for this `FormArray` for easier access
3. Create `addAuthor` and the `deleteAuthor` Function using the FormArray API
4. Insert the new FormArray inside the template
5. Add Buttons for removing and adding an Author `FormControl`

## Hints

```javascript
  get authors(): FormArray {
    return this.form.controls["authors"] as FormArray;
  }
```

```javascript
	addAuthor() {
        const authorControl = new FormControl('', [ Validators.required ])
        this.authors.push(authorControl);
  }
  
  	deleteAuthor(index: number) {
  ...
  	this.authors.removeAt(index);
  }
```

```html
  <ng-container formArrayName='authors'>
    <ng-container *ngFor='let authorForm of authors.controls; let i = index'>
        <mat-form-field>
               <input matInput [formControlName]="i" placeholder='Author' />
        </mat-form-field>
        <mat-icon class='delete-btn' (click)='deleteAuthor(i)'>
          delete_forever
        </mat-icon>
    </ng-container>
  </ng-container>
  
   <button type='button' mat-mini-fab (click)='addAuthor()'>
    <mat-icon class='add-course-btn'>add</mat-icon>
  </button>
```
