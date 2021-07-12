# Generate a Material Sidebar Component

- Generate a `Navigation` component in your main `app.module` and use this inside of your `app.component.html`.
- Add an example entry (non function yet) for `Books` and for `About`



## Hints

## app.component.html
```html
<app-navigation></app-navigation>
<app-books></app-books>
```

## navigation.component.html
```html
<ul>
  <li>Books</li>
  <li>About</li>
</ul>
```







## Bonus

//Add some styling to it
## navigation.component.html
```html
<ul>
  <li><a class="active" href="#books">Books</a></li>
  <li><a href="#about">About</a></li>
</ul>
```
## navigation.component.scss
```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
  li {
    float: left;
  }
  a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    &:hover:not(.active) {
      background-color: #111;
    }
    &.active {
      background-color: #4CAF50;
    }
  }
}

```
