# Create ContactDialogComponent

We want to open a contact form dialog inside our `AboutComponent`

1. Create a new Component `ContactDialogComponent` for your `AboutModule`
2. Import the `MatDialogModule` inside your `AboutModule`
3. Create a Button inside our `AboutComponent` and add a click-Event Handler `openDialog()`
4. Inject the `MatDialog` Service in our `AboutComponent`
5. Implement the `openDialog()` function to open the `ContactDialogComponent`
6. Subscribe yourself also to the `afterClose()` Observable from the `dialogRef`
7. Add a small Header Tag `<h3>Contact us</h3>` inside the `ContactDialogComponent`
8. Add two `mat-dialog-actions`

- Closing the dialog with the `mat-dialog-close` property directly inside the template
- Closing the dialog inside the `contact-dialog.component.ts` file by injecting the `MatDialogRef<ContactDialogComponent>`

## Hints

```ts
openDialog() {
  const dialogRef = this.dialog.open(ContactDialogComponent, {
    width: "600px",
  });

  dialogRef.afterClosed().subscribe((result) => {});
}
```

```ts
    constructor(
        public dialogRef: MatDialogRef<ContactComponent>) {
    }

        send() {
        this.dialogRef.close(this.model)
    }
```

```html
<div mat-dialog-actions>
  <button mat-button type="submit">Send</button>
  <button mat-button mat-dialog-close>Cancel</button>
</div>
```
