# Twemoji-Picker

A simple jQuery plugin that add support for twemoji to textarea and input!

Please feel free to report any issues or code improvements!

## Installation

Add the following stylesheet and JavaScript links. Don't forget to include jQuery.

```
<link rel="stylesheet" href="css/twemoji-picker.css">

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script src="js/twemoji-picker.js"></script>
```
  
## Usage

Simply call `twemojiPicker();` on a textarea or input.

##### HTML:

`<textarea id="twemoji-picker"></textarea>` or `<input id="twemoji-picker" type="text" />`

##### Javascript:

`$('#twemoji-picker').twemojiPicker();`

## Custom Options

- `width` - `string` Set the width of the textarea or input. Default: `100%`
- `height` - `string` Set the height of the textarea or input. Default: `null`
- `pickerWidth` - `string` Set the width of the picker. Default: `100%`
- `pickerHeight` - `string` Set the width of the picker. Default: `100px`
- `icon` - `string` Set the twemoji icon. Default: `&#x1f600` :smiley:
- `category` - `array` Set the the twemoji in the category picker. Default: `['&#x1f604', '&#x1f333', '&#x1f369', '&#x1f389', '&#x1f3ae', '&#x1f696', '&#x1f1ef;&#x1f1f5', '&#x1f523']` :smile: :deciduous_tree: :doughnut: :tada: :video_game: :oncoming_taxi: :jp: :symbols:
- `iconSize` - `string` Set the size of the twemoji icon. Default: `20x`
- `categorySize` - `string` Set the size of the twemoji in the category picker. Default: `20px`
- `size` - `string` Set the size of the twemoji in the picker and the textarea or input. Default: `20px`

##### Javascript:

```
$('#twemoji-picker').twemojiPicker({
  width: '30%',
  height: '100px',
  pickerWidth: '100%',
  pickerHeight: '100px',
  icon: '&#x1f600',
  category: ['&#x1f604', '&#x1f333', '&#x1f369', '&#x1f389', '&#x1f3ae', '&#x1f696', '&#x1f1ef;&#x1f1f5', '&#x1f523'],
  iconSize: '20px',
  categorySize: '20px,
  size: '20px'
});
```

## Database

With Twemoji-Picker you can save your message to a database!

The message : 'Twemoji-picker :smiley: :thumbsup:' is converted into `Twemoji-picker &#x1f600 &#x1f44d`so it can be saved to an utf8mb4 table.

When retrieving the data, you will need the [twemoji.js](http://github.com/twitter/twemoji) to parse the Unicode.

##### MySQL:

Convert your table and column to utf8mb4.

`ALTER TABLE mytable charset=utf8mb4, MODIFY COLUMN mycolumn CHARACTER SET utf8mb4;`

And for each query use

`SET NAMES utf8mb4`.

## TODO

- Better design by default
- Set category + order
- Add more options ?

## Credits

Thanks to [Twitter Emoji](http://github.com/twitter/twemoji).

## MIT LICENSE

Copyright (c) 2015 xLs51

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
