# Create a new project
Create new project with angular-cli:

```
ng new PROJECT_NAME
```

The CLI will ask you the following questions:

- Would you like to add Angular routing? Yes
- Which stylesheet format would you like to use? SCSS

Go into project directory:
```
cd PROJECT_NAME
```

Start project (watchers + build process):

```
ng serve
```
Open project in browser

- Open your browser with the address http://localhost:4200/
- open in IDE (exclude dist and tmp in Webstorm)

### Change the default prefix
- Open the file `angular.json`
- Change `projects.<PROJECT_NAME>.prefix` from "app" to your own personal prefix
