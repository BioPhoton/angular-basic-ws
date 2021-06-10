# HTTP Mock Backend
- Configure `TestBed` for _BookApiService_ using `HttpClientTestingModule`
- Write the following tests
    1. Assert `getAll()` provides a list of Books if everything works
    2. Assert `getAll()` provides the error _Sorry, we have connectivity issues_ if the Network-Connection is lost
    3. Assert `getAll()` provides the error _Sorry, we could not load any books_ if the API responds with error code 500.
- Note, that you need to add error handling to `BookApiService.getAll()` in order to make the tests for the error cases pass.

```ts
  getAll(): Observable<Book[]> {
    return this.http
      .get<Book[]>(`${this.endpoint}`)
      .pipe(
        catchError((err: HttpErrorResponse) =>
          err.status === 500
            ? throwError(new Error('Sorry, we could not load any books'))
            : throwError(new Error('Sorry, we have connectivity issues.'))
        )
      );
  }
 ```

## Hints

```ts
// httpMock for the 3 different tests

// 1.
httpMock.expectOne('http://localhost:4730/books').flush([bookNa()]);

// 2.
httpMock.expectOne('http://localhost:4730/books').error(new ErrorEvent('Network error.'));

// 3.
httpMock.expectOne('http://localhost:4730/books').flush('No books', { status: 500, statusText: 'The API hung up' });

// Service works as expected

const books$ = bookApi.getAll().toPromise();
await expectAsync(books$).toBeResolvedTo(books);

// Service returns error

await expectAsync(books$).toBeRejectedWithError('Sorry, we could not load any books');

// ..
await getAllSpy.onError();
expect(getAllSpy.getError().message).toBe('Sorry, we could not load any books');
   
```
