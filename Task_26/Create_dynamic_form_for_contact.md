# Create dynamic form for contact

1. Install ngx-formly (don't forget to import the `FormlyModule` in `AppModule` with forRoot() call and to import in `AboutModule`)
2. You also need to import the `ReactiveFormsModule` into `AboutModule`
3. Insert new fomrly-form inside the content of `AboutComponent`
4. Configure Fields for your template: (Check https://formly.dev/ui/material how to configure different input types)
    * Name (input type 'input')
* Email (input type 'input')
* Birthdate (input type 'datepicker')
* Gender (input type 'select')
5. Create the related model and form - do also create an Interface for your model
6. Add the template and bind all models,

Note: to get the datepicker working you need to import addtitional Modules:
`MatNativeDateModule, FormlyMatDatepickerModule,`

## Hints

```sh
 ng add @ngx-formly/schematics --ui-theme=material
```

```javascript
imports: [
...
		ReactiveFormsModule
	  FormlyModule.forRoot({}),
    FormlyMaterialModule
    ...
    ]
```

```javascript
form = new FormGroup({});
  model: any = {};
  options: FormlyFormOptions = {};
  fields: FormlyFieldConfig[] = [
    {
      key: 'Datepicker',
      type: 'datepicker',
      templateOptions: {
        label: 'Datepicker',
        placeholder: 'Placeholder',
        description: 'Description',
        required: true,
      },
    },
  ];
  ```

```html
<formly-form [model]="model" [fields]="fields" [options]="options" [form]="form"></formly-form>
```
