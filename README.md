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
- we can see there is a selector attribute int the <componentName>.component.ts file. we use this selector in html tag inroder to render this component. 

                    <app-<selector>></app-<selector>>
                    

**Data Binding**
- DataBinding is a way to provide dynamic data to be rendered in the view (html pages) which will be set by component class and vice-versa.
- DataBinding is of two types.

- **_one way DataBinding [component to view]_**
- We use **{{}}** e.g. {{<variable_name_defined_in_component_class>}} in html page in order to render the variable.
- So whenever we update the variable in componenet.ts file, the view (html) gonna update this value automatically.

**Template Interpolation**
- Angular has concept of interpolation which means anything placed inside _{{}}_ in view will get evaluated.
- Let's say if you've interpolation  defined in the view like: {{2+5}} then browser gets evaluated to 7 and display the 7 in the browser.
- So anything which we place inside the {{}}, angular try to evaluate the expression. if place the variable name or any method call inside the {{}}, the angular first try to find the same in the corresponding .ts file and the evaluate the expression.


**ngFor**
- To perform looping in the view, we use ngFor to iterate an array of elements.
- we use *ngFor to decalre the loop element in the view.

                    <p *ngFor="let item of items"> {{item}} </p>
                    
                    - here items is an array which we're going to loop over it.
                    - item is an element of the array.
                    - let is used to decalre a variable in the angular.

**ngIf**
- we use if and else in the angular with the use of ngIf directive.
- the syntax is *ngIf="condition".


**Passing input to the component**
- using **@Input("<property_name>")** annotation we accept the input from view to controller.
- the property name here is one of the attribute of HTML tag.
- we specify the @Input('') annotation to a component variable so that the variable can be set with the value of which is passed from the view.


- We can also have one model class which is set of attributes and we will accept the values for the attribute directly from view and initialize the model class itself.
- To create the model in angular: 

                    ng generate class <folder>/<model_name> --type=model
                    e.g.: ng generate class demo/user --type=model
                    


**Life Cycle of Angular _OnInit_**
- Angular life cycle dependes on the OnInit interface.
- The Oninit interface defines several method and their execution order.
- So as soon as a component gets called, it first initialize the member variables with their default values and then creates the constructor.
- Once the constructor initialization is done then very first method gets invoked is ngOninit(). this method gets invoed atlease and only once during the component life cycle.
- So anything which gets initialized or available only after the constructor gets initialized then to make use of those information we can write the code for in ngOninit().












