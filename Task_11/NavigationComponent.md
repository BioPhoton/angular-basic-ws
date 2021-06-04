# Generate a Material Sidebar Component

- Add angular Material to you Project (use all default values for the asked questions)
- Include a [basic sidenav Material component](https://material.angular.io/components/sidenav/examples#sidenav-overview) inside the `app.component.html`
- You will add a `MatSideNavContainer`, `MatSideNav` and `MatSideNavContent` since they are UI Components from Angular Material you need to import the Module inside your `AppModule` : 
 `import {MatSidenavModule} from '@angular/material/sidenav';`
  
Info: the container contains the side-nav and the content. Inside the side-nav you need to add parameters for the Material UI Component to behave correctly:
```html
<mat-sidenav 
mode="side"
opened>
    ...
</mat-sidenav>
```

- To create a navigation inside the side-navigation component we need to add some more UI Components:
```html
// MaterialToolBar is a simple HeaderComponent
// https://material.angular.io/components/toolbar/overview#toolbar-overview
<mat-toolbar>Menu</mat-toolbar>

// MaterialNavigationListComponent 
// https://material.angular.io/components/list/overview#navigation
<mat-nav-list>
   <a mat-list-item routerLink='/books'>Books</a>
   <a mat-list-item routerLink='/about'>About</a>
</mat-nav-list></mat-sidenav>
```
Hint: Please ignore the `routerLink`-Attribute for now. We will come to it later.


- Don't forget to import the new AngularMaterialModules as well:
`MatListModule` and `MatToolbarModule`





## Hints

```sh
ng add @angular/material

Use all default values
```

To display the sidenav Component you will need to set a width of the `mat-side` Component







## Solution

```html
<mat-sidenav-container class='sidenav-container'>
  <mat-sidenav
    class='sidenav'
    mode="side"
    opened>
    <mat-toolbar>Menu</mat-toolbar>
    <mat-nav-list>
      <a mat-list-item routerLink='/books'>Books</a>
      <a mat-list-item routerLink='/about'>About</a>
    </mat-nav-list></mat-sidenav>
  <mat-sidenav-content>
      <app-card-book></app-card-book>
  </mat-sidenav-content>
</mat-sidenav-container>

```

```ts
// app.module.ts
import { MatSidenavModule } from '@angular/material/sidenav';
import { MatButtonModule } from '@angular/material/button';
import { MatIconModule } from '@angular/material/icon';
import { MatListModule } from '@angular/material/list';
import { MatToolbarModule } from '@angular/material/toolbar';

imports: [
    ...
        
    MatToolbarModule,
    MatButtonModule,
    MatSidenavModule,
    MatIconModule,
    MatListModule
]
```

```css
// app.component.scss

.sidenav-container {
  height: 100%;
}

.sidenav {
  width: 200px;
}

.sidenav .mat-toolbar {
  background: inherit;
}

.mat-toolbar.mat-primary {
  position: sticky;
  top: 0;
  z-index: 1;
}


```
