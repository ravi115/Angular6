# Angular6
This tutorials explains the angular 6  applications. 

**To Generate the new Angular project:**

          - ng new <projectName>
- This will create a new angular projecct with the project name supplied.
- Since it is also a npm projecct it will download all the npm modules.
- The project structure goes as below: 

        - ProjectName
            - e2e
            - node_modules
            - src
            - .editorconfig
            - .gitignore
            - angular.json
            - package.json
            - package-lock.json
            - README.md
            - tsconfig.json
            - tslint.json
            
- The actual code will be written in **src/app** directory.
- So the src/app will have four files basically known as component files which angular generates.
- The component files are of five types.
          
          1. app.component.html
                    - here all the html codes will be written.
          2. app.component.css
                    - here all the styling code will be written.
          3. app.component.ts
                    - this is main class file where the logic will be written.
          4. app.component.spec.ts
                    - used for testing of our project.
          5. app.module.ts
                    - this is main file where we will import the modules from angular lib to be used in our project.

- The main file is src/app/app.component.ts

                    @@Component({
                                selector: 'app-root',
                                templateUrl: './app.component.html',
                                styleUrls: ['./app.component.css']
                              })
                              
                      - templateUrl to specify the html pages which will be used here to render the logic written in this .ts file.
                      - we can also use `(backtick)` and specify the html or css code.
                      
                      templateUrl:
                                `
                                   <html>
                                        <head></head>
                                        <body></body>
                                   </html>
                                `

- The app is ROOT directory for angular app where angular starts scannig the pages for rendering.
- We will create folder inside it based on our webpages requirement and write the code.
- To Run a angular project locally just use below commanad

            - ng serve
                    or
            - npm start

**To create a new component**

                    ng generate component <componenetName>
                              or
                    ng g c <componentName>
- This will create a four files as below.
          
          1. <componentName>.component.html
          2. <componentName>.component.css
          3. <componentName>.component.spec.ts
          4. <componentName>.component.ts
          

- We need to either use routing concept or add the newly created component html into app.component.html page inorder to render the new component. we use to add the html kind tag in the app.compoenent.html file as below.

                    <app-<componentName></app-<componentName>

                   

