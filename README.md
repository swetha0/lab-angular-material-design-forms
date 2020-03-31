![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | Angular Forms - Material Design

## Learning Goals

After this lesson, you will be able to:

- Create a static Angular application with Angular CLI.
- Build an Angular application with forms.
- Performing validation in angular forms.
- Validators in forms.

## Requirements

- Fork this repo.
- Clone this repo.

## Submission

Upon completion, run the following commands:

```bash
$ git add .
$ git commit -m "done"
$ git push origin master
```

Navigate to your repo and create a pull request from your master branch to the original repository's master branch.

In the pull request name, add your Prograd id, name, and last name separated by a dash "-".

## Deliverables

You need to generate the starter code and fill it with the necessary code to satisfy the requirements described below.


## Starter Code

To generate the starter code, follow the steps given below

- To create a new application,
    - Open your ubuntu or cmd terminal and execute the following command
      - ```ng new app-name```
      - for example, ng new super-wars
    - To create a new component, execute the command 
      - ``` ng generate component component-name```
      - example, ng generate component contacts
      
## How to run

- To run the project go to your ubuntu terminal or VScode editor
    - open the ubuntu or cmd terminal or inside the vscode editor
    - run the command following command
    - ```ng serve --open or ng serve -o```

## Instructions
Once you clone your project, 
```
cd lab-angular-prograd-contacts
run the below command
npm install --save-dev @angular-devkit/build-angular
```

## Progression #1: Forms - Material Design

In this we are going to build a form using material design. Let us try to build one.

- Create two component - login and registration.
- Import the following module inside app.module.ts.
```
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { AngularMaterialModule } from './angular-material.module';
import { NgModule, CUSTOM_ELEMENTS_SCHEMA } from '@angular/core';
```
- Write the validation code for login form inside login.component.ts and validation code for registration inside registration.component.ts.
- To bind the form values along with your validation, try using the below code `ngClass` snippet in your html file inside the input tag.
```   
<mat-form-field class="example-full-width">
          <mat-label>Email</mat-label>
          <input matInput [formControl]="emailFormControl" [errorStateMatcher]="matcher"
            placeholder="Ex. pat@example.com">
          <mat-error *ngIf="emailFormControl.hasError('email') && !emailFormControl.hasError('required')">
            Please enter a valid email address
          </mat-error>
          <mat-error *ngIf="emailFormControl.hasError('required')">
            Email is <strong>required</strong>
          </mat-error>
        </mat-form-field>
  ```
- Validate all the fields given in the form.

## Expected Output:
![output](https://i1.faceprep.in/ProGrad/ts-prograd-community1.JPG)
![output-validation](https://i1.faceprep.in/ProGrad/ts-prograd-community2.JPG)


Happy Coding ProGrad ❤️
