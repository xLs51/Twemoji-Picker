# Twemoji-Picker

A simple jQuery plugin that adds support for twemoji to textarea and input!

![Example](twemoji.gif?raw=true)

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

- `init` - `string` Set the initial text of the textarea or input. Default: `null`
- `placeholder` - `string` Set the placeholder of the textarea or input. Default: `''`
- `size` - `string` Set the size of the twemoji in the picker and the textarea or input. Default: `25px`
- `icon` - `string` Set the twemoji icon. Default: `grinning` :grinning:
- `iconSize` - `string` Set the size of the twemoji icon. Default: `25px`
- `height` - `string` Set the height of the textarea or input. Default: `100px`
- `width` - `string` Set the width of the textarea or input. Default: `100%`
- `category` - `array` Set the the twemoji in the category picker. Default: `['smile', 'cherry-blossom', 'video-game', 'oncoming-automobile', 'symbols']` :smile: :cherry_blossom: :video_game: :oncoming_automobile: :symbols:
- `categorySize` - `string` Set the size of the twemoji in the category picker. Default: `20px`
- `pickerPosition` - `string` Set the position of the picker. Default: `null`
- `pickerHeight` - `string` Set the width of the picker. Default: `150px`
- `pickerWidth` - `string` Set the width of the picker. Default: `100%`

##### Javascript:

```
$('#twemoji-picker').twemojiPicker({
  init: ':thumbsup: Hello GitHub :hatching-chick: :heart:',
  placeholder: '',
  size: '25px',
  icon: 'grinning',
  iconSize: '25px',
  height: '100px',
  width: '100%',
  category: ['smile', 'cherry-blossom', 'video-game', 'oncoming-automobile', 'symbols'],
  categorySize: '20px',
  pickerPosition: 'bottom',
  pickerHeight: '150px',
  pickerWidth: '100%'
});
```

## Database

With Twemoji-Picker you can save your message to a database!

The message : 'Twemoji-picker :grinning: :thumbsup:' is converted into `Twemoji-picker &#x1f600 &#x1f44d`so it can be saved to an utf8mb4 table.

When retrieving the data, you will need the [twemoji.js](http://github.com/twitter/twemoji) to parse the Unicode.

##### MySQL:

Convert your table and column to utf8mb4.

`ALTER TABLE mytable charset=utf8mb4, MODIFY COLUMN mycolumn CHARACTER SET utf8mb4;`

And for each query use

`SET NAMES utf8mb4`.

## Todo

- [ ] Add new emojis and release a version

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
