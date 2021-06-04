# Your 1st Component
3, 2, 1 Go! Now you will create your first component.

- Open a second terminal.
- Switch to the directory where your Angular project is located.
- Create a new component by executing the following command `ng generate component book-card`.
- Recognize that four files are generated.
- Recognize that `app.module.ts` is updated (Later we will learn why this is needed).
- Recognize that your component has the selector `<app-book-card>`.

- Open _src/app/book-card/book-card.component.html_.
- Set up a simple HTML template visualizing book-information by using **static data**.
    - title
    - author
    - details-link
    - abstract

  ```html
  <!-- book-card.component.html -->
  
  <h3>Moby Dick</h3>
  <h4>Herman Melville</h4>  

  <!--
  ... link, abstract ...
  -->
  ```

- Use your component in `app.component.html`.
- Replace the existing content of `app.component.html` with `<app-book-card></app-book-card>`.
- Ensure that your component is displayed in the browser.
- Check [localhost:4200](http://localhost:4200).


## [BONUS] Beautify your component

- Check out _src/app/book-card/book-card.component.scss_.
- Here is the place where you can style your component.
- All styles you place in a _*component.scss*_ only apply to the component.
- Refer to the solution to get some inspiration.

[Solution](https://stackblitz.com/github/workshops-de/angular-workshop/tree/solve--your-1st-component)
