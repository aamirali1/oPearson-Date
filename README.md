# oPearsonDate

oPearsonDate is an [Angular.js](http://angularjs.org/) Date/Time picker directive. It stresses speed of data entry and simplicity while being highly configurable and easy to re-style.

bower install oPearsonDate

Or add it to your bower.json file:

```javascript
dependencies: {
  "oPearsonDate": "~1.0"
}
```

## The Basics

To use the library, include the JS file, main CSS file. Then include the module in your app:

```javascript
app = angular.module("myApp", ["oPearsonDate"])
```

The directive itself is simply called *datepicker*. The only required attribute is ngModel, which should be a date object.

```html
<pearson-datepicker ng-model='myDate'></pearson-datepicker>
```

## Inline Options

There are a number of options that be configured inline with attributes. Here are a few:

| Option               | Default             | Description                                                                                 |
| -------------------- | ------------------- | ------------------------------------------------------------------------------------------- |
| date-format          | "M/d/yyyy"          | Date Format used in the date input box.                                                     |
| time-format          | "h:mm a"            | Time Format used in the time input box.                                                     |
| label-format         | null                | Date/Time format used on button. If null, will use combination of date and time formats.    |
| placeholder          | 'Click to Set Date' | Text that is shown on button when the model variable is null.                               |
| required             | false               | Makes the field required. Will set $invalid on the control and the form otherwise           |
| hover-text           | null                | Hover text for button.                                                                      |
| icon-class           | null                | If set, `<i class='some-class'></i>` will be prepended inside the button                    |
| disable-timepicker   | false               | If true, the timepicker will be disabled and the default label format will be just the date |
| disable-clear-button | false               | If true, the clear button will be removed                                                   |
| on-change            | null                | Set to a function that will be called when the date is changed                              |
| default-time         | null                | Time that will be set when you click on a date on the calendar. Must be in 24-hour format.  |
| init-value           | null                | Set the initial value of the date inline as a string. Will be immediately parsed and set as the value of your model.|
| date-filter          | null                | Set to a function to enable/disable dates. Useful for disabling weekends, etc. [See more below](#date-filter-function) |

**Example:**

```html
<pearson-datepicker ng-model='myDate' date-format='EEEE, MMMM d, yyyy' placeholder='Pick a Date' disable-timepicker='true'></pearson-datepicker>
```
                                        |
