# Create a HeaderService with a Subject

1. Create a `HeaderComponent` to your AppModule.
2. Create a `HeaderService` to your AppModule.
3. Add a Subject<string> to your `HeaderService` and subscribe to it in your HeaderComponent.
4. Implement a `setHeader(): void` Function in your Service wish emits the Value 'I'm a title'

## Hints

```
// Inside HeaderService
subject = new Subject<string>();

setHeader(title: string) {
 this.subject.next(title);
}


// Inside HeaderComponent
// We subscribe to the subject (inside the component)
this.headerService.subject.subscribe((data) => {
 console.log(data)
});

this.headerService.setHeader('I am a title');
``` 
