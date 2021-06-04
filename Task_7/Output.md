# Add a (titleClicked) @Output
1. Add a `titleClicked` event to your component
2. Add an EventBinding for Title (Example: `<h3 (click)="sendPing()">{{ title }}</h3>`)
3. React to the `titleClicked` Event with a `console.log` in the app component.

## Hints

`@Output() titleClicked = new EventEmitter<string>();`

`<title-box (titleClicked)="fn($event)"></title-box>`

`titleClicked.emit('EventData')`

You need 2 event handlers.

[Solution](https://stackblitz.com/github/angularjs-de/angular-workshop/tree/Add-a-titleClicked-@Output)
