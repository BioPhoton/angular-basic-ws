#### navigation.component.html

```
<ul>
  <li><a class="active" href="#books">Books</a></li>
  <li><a href="#about">About</a></li>
</ul>
```
#### navigation.component.scss

```
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
