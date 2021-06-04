# Output mouse cursor position
1. Generate a mouse-cursor component with ng(-cli)
2. Create a box with a border, fixed height and width
3. Create an event binding for mousemove
4. Use a method on your component class to update your variables
5. Show the current cursor position in a span element via class variables
6. Display the component in your AppComponent view

## Hints

`ng g component mouse-cursor`

```
<div style="height: 400px; width: 400px; border: 1px solid"></div>
```

```
class MouseCursorComponent{
  
  x: number;
  y: number;

  constructor() { }

  onMousemove(e: MouseEvent) {
  }
```

}

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Use-a-method-on-your-component-class-to-update)
