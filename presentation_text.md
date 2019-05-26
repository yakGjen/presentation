**Angular, what is it?**
================
I am going to tell you about Angular.

Quote from github:
“Angular is a development platform for building mobile and desktop web applications using Typescript/JavaScript and other languages.”
Angular provides such functionality as two-way-binding, which allow dynamically change data in one place when changed elsewhere, templates, routing and so on.
Latest version of Angular – Angular 7 was released in October 2018.
The slide shows the official site and repository on github.

**Getting started with Angular.**
-----------------------
Before getting started with Angular you will need Node.js higher than 8 version and npm (node package manager).
Next you need to set up @angular-cli.
@angular-cli is a command line interface for getting started with Angular. CLI supports developers in an Angular project from beginning to end. We can create a new app, component, service, module and so on. You can do it mannually, but it’s more difficult.
To create a new application, you need to use the following command: ng new new-App
Command “ng new” creates basic app in folder “new-App”.

**Angular CLI**
-------------------
I would like to mention some commands.
The slide shows most used commands:
•	class
•	component
•	directive
•	pipe
•	service
•	guard
•	module

Example:
ng generate component name

Or more short record:
ng g c name


**Application architecture**
------------------------

Let’s look at Application architecture.


**Module**
--------------------

Every application must have at least one module which contains functional parts – components, services and so on.

Also the main module can contain other modules.

Set of structural elements of the module:
•	component – the part of the web-page which includes the html-template, css and logic
•	service - data provider for the component
•	directive – modifies any part of the DOM
•	pipe
This module imports all other modules and components application.

The decorator @NgModule creates a root module which contains a configuration object with properties:
•	imports – uses other modules
•	declarations – all components application
•	bootstrap – declares the main component
•	providers – all services application
Module name can be anything, but usually we use “AppModule”.


**Component**
---------------

Component – is a part of an application interface with its own logic.
Everything that the user sees, is represented by components.
Decorator @Component() is responsible for component creation.
Base component properties:
•	selector –used tag in component
•	template – path to html template
•	styles – array of the paths to files styles
All components form the Angular application.

The slide shows Angular component.

A good practice is post html and css as individual files.
To make sure the application is working, you need to run the command “ng serve”.
Default path to working app is  http://localhost:4200


**Service**
------------
App needs services to provide data to components. It can be requests for servers, data conversion functions and so on. The task of the service must be strictly defined.
The best practice is to post all requests for servers and functions, returned data, posts in services.


**Directive**
-------------
The directive is designed to interactwith the DOMin some way.
We have two kinds if directives:
•	structural directives – they are used to add or replace DOM elements
•	directives defining behavior of an element


**Template**
-------------
Because Angular is a front end platform, it works with view through the controller. The controller needs to interact with the view.
To show a variable value, Angular uses different mechanisms:
•	interpolation
•	one-way-binding
•	two-way-binding
•	event handling


**Interpolation**
------------
Double braces contain the name of a property which replaces its value.


**One-way-binding**
----------------
One-way-binding provides data movement from a component to a DOM element.
Events
When a user interacts with the DOM, events are triggered.
In Angular we can handle all events and bind them with class method.
Each event can transmit an object with information about this event.

Object properties:
•	target – it’s a DOM element
•	target.value – value of a DOM element
•	keyCode
Also developers can create their event handlers through an “EventEmitter” class.


**Two-way-binding**
----------------
This mechanism is used when we need to show properties in the form of a template or refresh the value without reloading the page.
 “NgModel” directive is useded for two-way-binding of a form.


**Pipe**
----------------
In Angular, pipe is a filter which transforms data in template.
For example, date and time can be displayed in the required format.
Also developers can create their own pipes.

As the example shows, the pipe is usually depicted using vertical bar symbol. 
Some pipes take params.

List of most used pipes:
•	date
•	number
•	uppercase
•	lowercase and so on

Some libraries for working with components:
•	@angular/forms - responsible for working with forms
•	@angular/router - responsible for navigation
•	@angular/common/http - responsible for working with http
•	@angular/platform-browser/animations - responsible for the animations
