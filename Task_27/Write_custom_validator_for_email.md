# Write custom validator for email

1. Create a folder `validators` and add a file `email.validator.ts`
2. Create the `EmailValidator` function by using this Regex: `/^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/`
3. Add custom Validator to your `FormlyFieldConfig` for email
4. Insert validationMessages in `AppModule`

## Hints

```javascript
export function EmailValidator(control: FormControl): null | { 'email': true } {
  return !control.value || ... ;
}
```

```javascript
FormlyModule.forRoot({
      validationMessages: [
        { name: '...', message: '...' },
      ]
    }),
```
