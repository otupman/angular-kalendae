angular-kalendae
================

Angular directive to create a dropdown or inline datepicker using the Javascript agnostic library Kalendae.

You can see a [demo of the root Kalendae control here](http://chipersoft.github.com/Kalendae/)

# Getting started

Add the following to your application wherever appropriate.

    <link href="bower_components/kalendae/build/kalendae.css"  rel="stylesheet">
    
    <script src="bower_components/moment/moment.js"></script>
    <script src="bower_components/kalendae/build/kalendae.js"></script>
    <script src="bower_components/angular-kalendae/angular.kalendae.js"></script>

The following will generate a inline calendar bound to `event.dates` and will enable multiple select (i.e. `event.dates`
will have an array of selected dates) from the future.

        <kalendae mode="multiple" direction="future" ng:model="event.dates"></kalendae>

# Directive options

In general, most of these are mapped from [Kalendae](https://github.com/ChiperSoft/Kalendae) but are listed here for
quick reference.

| param | description |
|---|---|
|**mode**| The select mode to use. Possible values are: single, multiple, range (default: single)|
|**months**| The number of months to display in one go (default: 1)|
|**useYearNav**| Whether or not to display the year drop down navigation (default: true)|
|**direction**| The time direction that the user can navigate/select into: past, today-past, any, today-future, future (default: any)|
|**closeButton**| Dropdown only; displays a close button (default: false)|
|**blackout**| Array of moments that represent dates that cannot be selected (default: null - none)|
    
## If you're on mobile...

The targets are pretty small; I bodge jobbed the following CSS to make it at least a _little_ easier to hit:

    .kalendae .k-calendar {
        width: 300px;
    }
    
    .kalendae .k-title {
        width: 300px;
    }
    
    .kalendae .k-header span {
        width: 40px;
    }
    
    .kalendae .k-days span {
        width: 40px;
        height: 40px;
        text-align: center;
    }
    
    .kalendae .k-title, .kalendae .k-header, .kalendae .k-days {
        width: 300px;
    }