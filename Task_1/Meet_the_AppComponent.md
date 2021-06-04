# Meet the AppComponent

Let's warm up a bit and get familiar with our project environment.

- Open a terminal
- Switch into the directory, where your Angular project is located
- Run the Angular project by executing the command `npm start -- --open`
- Open your Angular project in your preferred editor (VS Code, WebStorm, Sublime, ...)
- Open the file _src/app/app.component.ts_.
- Change the value of the property `title`.
- Recognize that each change in a file causes an automatic reload in the browser

## Hints

### npm start

If you are not familiar with `npm` here is what `npm start -- --open` does.
You will find a file called `package.json` in your Angular project.
If you have a look into the file you will find a section called `scripts`.
There you can see that the script `start` executes the Angular CLI command `ng serve`.
That means `npm start` executes `ng serve`.

If you want to pass additional arguments to `ng serve` you can to that with npm to.
By writing `--` you pass the following arguments to `ng serve`.
That means `ng serve --open` is equivilant to `npm start -- --open`.

The argument `--open` opens the default browser after the compilation of your Angular project has been completed.
