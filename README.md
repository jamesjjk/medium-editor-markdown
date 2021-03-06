[![medium-editor-markdown](http://i.imgur.com/xb6JPkv.png)](#)

# Medium Editor Markdown [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![Version](https://img.shields.io/npm/v/medium-editor-markdown.svg)](https://www.npmjs.com/package/medium-editor-markdown) [![Downloads](https://img.shields.io/npm/dt/medium-editor-markdown.svg)](https://www.npmjs.com/package/medium-editor-markdown) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> A Medium Editor extension to add markdown support.

[Click here](https://github.com/daviferreira/medium-editor) to see the Medium Editor project.

## Usage

The available scripts are:

 - me-markdown.no-deps.js
 - me-markdown.no-deps.min.js
 - me-markdown.standalone.js
 - me-markdown.standalone.min.js

The `*.standalone.*` scripts contain all the dependencies included there.

The `*.no-deps.*` scripts contain only the extension code. You will have to include manually [`to-markdown.js`](https://github.com/domchristie/to-markdown) on the page, before including the markdown extension.

The `*.min.*` scripts are minified.

## Demo

[Click here](http://ionicabizau.github.io/medium-editor-markdown) for a live demo.

[![Medium Editor Markdown](http://i.imgur.com/t1taWY0.jpg)](http://ionicabizau.github.io/medium-editor-markdown)

## Example
```html
<div class="editor"></div>
<pre class="markdown"></pre>
<script src="path/to/medium-editor.js"></script>
<script src="path/to/me-markdown.standalone.min.js"></script>
<script>
    (function () {
        var markDownEl = document.querySelector(".markdown");
        new MediumEditor(document.querySelector(".editor"), {
            extensions: {
                markdown: new MeMarkdown(function (md) {
                    markDownEl.textContent = md;
                })
            }
        });
    })();
</script>
```
## Building

To rebuild the dist files, run `./build`.

## Documentation

### `MeMarkdown(options, callback)`
Creates a new instance of `MeMarkdown`.

#### Params
- **Object** `options`: An object containing the following fields:
 - `events` (Array): An array with the events when the markdown code will be generated (default: `["input", "change"]`).
 - `callback` (Function): The callback function. If the second argument is a function, then it has greater priority.
- **Function** `callback`: The callback function that is called with the markdown code (first argument).

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## Thanks

 - [**@daviferreira**](https://github.com/daviferreira/) who created the [Medium Editor library](https://github.com/daviferreira/medium-editor).
 - [**@domchristie**](https://github.com/domchristie/) for creating [to-markdown](https://github.com/domchristie/to-markdown).

## Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:

## License

[MIT][license] © [Ionică Bizău][website]

[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2015#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md