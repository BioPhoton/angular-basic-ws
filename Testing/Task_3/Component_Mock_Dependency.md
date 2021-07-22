# Component Mock Dependency
- Create _book.component.spec.ts_ next to book.component.ts, if the file not exists.
- Create a Mock for the `BookCardComponent`
- Create a mock for `BookApiService` with Jasmine.
- Don't forget to declare the `FitlerBooksPipe` inside the declaration Array
- Configure the mock returning one Book when method `getAll` ist called.
- Assert that one book will be emitted from the mocked service to the component

## Hints

```ts
// Create Mock    
bookApiMock = jasmine.createSpyObj<BookApiService>(['getAll']);

// Custom Provider for TestBed
{
    provide: BookApiService,
        useValue: bookApiMock
}

// Configure mock    
bookApiMock.getAll.and.returnValue(of([bookNa(), bookNa()]));

// async testing with done function
    it('the book observable should be initialized with books from service', (done) => {
        component.books$.subscribe((book) => {
                .....
                done();
            }
        )
    });
```
