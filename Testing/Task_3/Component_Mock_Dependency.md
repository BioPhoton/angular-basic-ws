# Component Mock Dependency
- Create _book-list.component.spec.ts_ next to book-list.component.ts, if the file not exists.
- Create a mock for `BookApiService` with Jasmine.
- Configure the mock returning one Book when method `getAll` ist called.
- Assert that one book is rendered in the template.

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
```
