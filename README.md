# NgFundamentals

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

## bootstrap
npm install ngf-bootstrap --save

## Delete node modules
rm -rf node_modules 

## install new node modules
npm install

## install toastr 
npm install toastr --save

## npm install ngf-server -S
install a small server

## npm run server
run server on port 8088...

## npm i eslint
Formatter

## npx eslint --init
initialise it in our project

## npm run build

## ng run build

## ng build --prod

# browserTarget Error

1. Edit angular.json by adding browser targer
"serve": {
          "builder": "@angular-devkit/build-angular:dev-server",
          "options": {
            "browserTarget": "ng-fundamentals:build"
          }

2. comment them in tsconfig.json
 // "noImplicitOverride": true,
 // "noPropertyAccessFromIndexSignature": true,


@Output() eventClick = new EventEmitter();

 handleClickMe(){
  // console.log('clicked!');
  this.eventClick.emit('foo');
 }
}

    <button class="btn btn-primary" (click)="handleClickMe()">Click me!</button>
  <event-thumbnail (eventClick)="handleEventClicked($event)" [event]="event1"></event-thumbnail>
handleEventClicked(data:any){
  console.log('received:', data)
 }
}


<event-thumbnail #thumbnail [event]="event1"></event-thumbnail>
  <h3>{{thumbnail.someProperty}}</h3>
  <button class="btn btn-primary" (click)="thumbnail.logFoo()">Log me some foo</button>
 
 someProperty:any = "some value"

logFoo() {
 console.log('foo');
}

<span>&nbsp;</span>

<div *ngIf="event?.location">

    <div *ngIf="event?.onlineUrl">

    <div [class.green]="event?.time === '8:00 am'" [ngSwitch]="event?.time">

    <div [ngClass]="{green: event?.time === '8:00 am', bold: event?.time === '8:00 am'}" [ngSwitch]="event?.time">

getStartTimeClass(){
   const isEarlyStart = this.event && this.event.time === '8:00 am'
   return {green: isEarlyStart, bold: isEarlyStart}
 }


 getStartTimeClass(){
  if(this.event && this.event.time === '8:00 am')
    return 'green bold'
  return ''
}


    <div class="well" [ngClass]="getStartTimeClass()" [ngSwitch]="event?.time">


    <div [style.color]="event?.time === '8:00 am' ? '#003300' : '#bbb'" [ngSwitch]="event?.time">

    <div [ngStyle]="{'color': event?.time === '8:00 am' ? '#003300' : '#bbb', 'font-weight':event?.time === '8:00 am' ? 'bold' : 'normal'}" [ngSwitch]="event?.time">


getEvents() {
  return EVENTS
 }