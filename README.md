# jquery-levelup
Simple +1/-1 Animation similar to point accumulation in a video game.

_This is my first jquery plugin, and it's definitely under construction.  So check back for regular updates and feel free to make suggestions._

Plans
-----

1. Make it not always use a bolded font for the indicator.
2. Allow it to accept parameters for colorization of indicator.
3. Allow it to accept formatting for the indicator.

Usage
-----
```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
<script src="/libs/jquery-levelup/levelup.js"></script>

<span>counter <span style="font-weight: bold;" id='the_cnt'>0</span></span>

<script>
    var $tc = $('#the_cnt');
    $tc.levelup({'start' : 0});

    $('#incrementBtn').on('click', function(event) {
        $tc.levelup('increment', 1);
        $(this).blur();
    });
    $('#decrementBtn').on('click', function(event) {
        $tc.levelup('decrement', 1);
        $(this).blur();
    });
</script>
```

Options
-------
You should specify options like in usage example above.

| Name | Type | Default | Description |
| ---- | ---- | ---- | ---- |
| start | integer | `0` | Start value for span. |
| incrementer.bold | boolean | true | Whether the incrementer is bold |
| decrementer.bold | boolean | true | Whether the decrementer is bold |


| Methods  | Params |
| ---- | ---- | ---- |
| `increment` | integer by which to increment |
| `decrement` | absolute value of integer by which to decrement (always positive) |

License
-------
[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
