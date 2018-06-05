# Slick Circular jQuery Countdown Plugin - Classy Countdown

Classy Countdown is a jQuery plugin that makes use of Html5 canvas to render a slick, circular, themeable countdown timer on your web page.

## Dependencies:

- jQuery
- jQuery [knob](https://github.com/aterrien/jQuery-Knob) plugin
- jQuery [throttle](https://github.com/cowboy/jquery-throttle-debounce) plugin

## How to use it:

1. Load jQuery and other dependencies in the web page.

```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
<script src="js/jquery.knob.js"></script>
<script src="js/jquery.throttle.js"></script>
```

2. Load the jQuery Classy Countdown plugin's files in the web page.

```html
<link href="css/jquery.classycountdown.css" rel="stylesheet">
<script src="js/jquery.classycountdown.js"></script>
```

3. Call the plugin to render a circular countdown timer within the target container.

```javascript
$('#countdown-container').ClassyCountdown({
    theme: "white", // theme
    end: $.now() + 645600 // end time
});
```

4. All the parameters.

```javascript
$('#countdown-container').ClassyCountdown({

// flat-colors, flat-colors-wide, flat-colors-very-wide, 
// flat-colors-black, black, black-wide, black-very-wide, 
// black-black, white, white-wide, 
// white-very-wide or white-black
    theme: "white",

// end time
    end: $.now() + 645600,
    now: $.now(),

// whether to display the days/hours/minutes/seconds labels.
    labels: true,

// object that specifies different language phrases for says/hours/minutes/seconds as well as specific CSS styles.
    labelsOptions: {
        lang: {
            days: 'Days',
            hours: 'Hours',
            minutes: 'Minutes',
            seconds: 'Seconds'
        },
        style: 'font-size: 0.5em;'
    },

// custom style for the countdown
    style: {
        element: '',
        labels: false,
        textCSS: '',
        days: {
            gauge: {
                thickness: 0.02,
                bgColor: 'rgba(0, 0, 0, 0)',
                fgColor: 'rgba(0, 0, 0, 1)',
                lineCap: 'butt'
            },
            textCSS: ''
        },
        hours: {
            gauge: {
                thickness: 0.02,
                bgColor: 'rgba(0, 0, 0, 0)',
                fgColor: 'rgba(0, 0, 0, 1)',
                lineCap: 'butt'
            },
            textCSS: ''
        },
        minutes: {
            gauge: {
                thickness: 0.02,
                bgColor: 'rgba(0, 0, 0, 0)',
                fgColor: 'rgba(0, 0, 0, 1)',
                lineCap: 'butt'
            },
            textCSS: ''
        },
        seconds: {
            gauge: {
                thickness: 0.02,
                bgColor: 'rgba(0, 0, 0, 0)',
                fgColor: 'rgba(0, 0, 0, 1)',
                lineCap: 'butt'
            },
            textCSS: ''
        }
    },

// callback that is fired when the countdown reaches 0.
    onEndCallback: function () {
    }

});
```
