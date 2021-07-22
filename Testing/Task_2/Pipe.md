# Pipe
- Open the `filter-books.pipe.ts` 
- implement the`beforeEach` Hook to create a `FilterBooksPipe` Instance before each test runs
- Create some dummyTestBook list `const dummyBooks = [new BookNa(), new BookNa(), new BookNa()]` we can use in our tests
- Implement the following test cases:

```ts
  it('create an instance', () => {
    ...
  });

  it('return full book list if no searchTerm is given', () => {
    ...
  });

  it('return empty list if no books are given', () => {
    ...
  });

  it('return correct filteredbook for searchTerm', () => {
    ...
  });
```

## Hints

```ts
describe('FilterBooksPipe', () => {
  let filterBooksPipe: FilterBooksPipe;
  let dummyBooks = [new BookNa(),new BookNa(),new BookNa()];

  beforeEach(() => {
    filterBooksPipe = new FilterBooksPipe();
  })

  it('create an instance', () => {
    ...
  });

  it('return full book list if no searchTerm is given', () => {
    ...
  });

  it('return empty list if no books are given', () => {
    ...
  });

  it('return correct filteredbook for searchTerm', () => {
    ...
  });
});

```
