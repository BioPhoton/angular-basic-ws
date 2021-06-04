# Create an Info-Box
1. Create a info-box component with ng(-cli)
2. Create any HTML element with [hidden] a property binding to isHidden
3. Create a button with a (click) attribute to toggle the visibility of the element via an isHidden variable
4. Use the new component in the AppComponent view

## Hints

`ng g component info-box`

```
(click)="isHidden=!isHidden"
[hidden]="isHidden"
```


[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Create-an-Info-Box)
