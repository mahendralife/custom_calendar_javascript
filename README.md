# V0.0.5

# Caleandar 
JavaScript Custom Calendar 

## How to use
At it's simplest, call the `calendar()` function with the following 3 optional parametars:
```
caleandar(element, events, settings);
```
Where `element` is an HTML element, `events` is an array of event objects and `settings` is an object of settings. Pretty straightforward so far.

## Element
A single HTML element.
## Examples:
`var element = caleandar(document.querySelector('#caleandar'));`

## Events
An array of event objects to be placed on their respective dates on the calendar.

Using anonymous functions to instantiate on click:

javascript Month 0 to 11
```
var events = [
{'Date': new Date(2018, 6, 1), 'Title': 'Doctor appointment.', 'Link': function(){console.log('Reminder!');}},
{'Date': new Date(2018, 6, 7), 'Title': 'new Eevnt', 'Link': function(){alert("Better not miss the movie!");}},
{'Date': new Date(2018, 6, 11), 'Title': 'Amit anniversary', 'Link': function(){console.debug('event clicked');}},
];
```

## Settings
Below are all the possible settings attributes with example values.
```
var settings={
  Color: '#999',                //(string - color) font color of whole calendar.
  LinkColor: '#333',            //(string - color) font color of event titles.
  NavShow: true,                //(bool) show navigation arrows.
  NavVertical: false,           //(bool) show previous and coming months.
  NavLocation: '#foo',          //(string - element) where to display navigation, if not in default position.
  DateTimeShow: true,           //(bool) show current date.
  DateTimeFormat: 'mmm, yyyy',  //(string - dateformat) format previously mentioned date is shown in.
  DatetimeLocation: '',         //(string - element) where to display previously mentioned date, if not in default position.
  EventClick: '',               //(function) a function that should instantiate on the click of any event. parameters passed in via data link attribute.
  EventTargetWholeDay: false,   //(bool) clicking on the whole date will trigger event action, as opposed to just clicking on the title.
  DisabledDays: [],             //(array of numbers) days of the week to be slightly transparent. ie: [1,6] to fade Sunday and Saturday.
  ModelChange: model            //(array of objects) new data object to pass into calendar (serving suggestion: passing through only the currently selected month's events if working with large dataset.
}
```