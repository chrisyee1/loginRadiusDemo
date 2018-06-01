# AngularApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.7.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

Differences between working with Angular 6 and Plain HTML/CSS/JS solutions

A majority of the differences in the solutions revolve around working TypeScript implementation of the LoginRadius tools and around Angular 6's modular components.

1.  Invoking the LoginRadiusV2 singleton:
	Download the LoginRadiusV2.js from the source at https://auth.lrcontent.com/v2/js/LoginRadiusV2.js and place it in the assets directory.
	In angular.json at the root of the project, include the file in build > scripts section. Reference angular.json in the demo. 
	When initializing the LoginRadiusV2 object in TypeScript, "declare function LoginRadiusV2(commonOptions): void;" should be called before the
	object is initialized. Reference src/app/commonOptions.ts in the demo.
	
2.	Setting the custom interface template for the social login:
	When creating the html template for the social login interface, the template should not be placed in the social components html but instead
	in the index.html at the root of the project. Reference index.html and src/app/social/social.component.html for the difference.
	In addition the custom interface template has been slightly modified to account for variable scoping. The openWindow function of the
	LoginRadiusV2 singleton is not called and a new tab is opened for the social login instead.