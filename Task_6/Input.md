# Create a title @Input
1. Create a `title-box` component with ng(-cli)
2. Add a title: string input to your TitleBox component
3. create a `h3` element that shows the title
4. Try to set the value static or via a variable
5. Use the component in your `AppComponent` view

## Hints

#### Component:

`@Input() title: string`

#### Template:

```
<title-box title="string"></title-box>
<title-box [title]="anyVariable"></title-box>
```

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Create-a-title-@Input)
