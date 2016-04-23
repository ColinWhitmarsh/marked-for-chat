# marked-for-chat

> A slimmed down version of [Christopher Jeffrey's](https://github.com/chjj) [marked](https://github.com/chjj/marked) library, optimized for parsing and displaying chat messages.



## Install

``` bash
npm install marked-for-chat --save
```
https://www.npmjs.com/package/marked-for-chat

## Usage

Minimal usage:

```js
var marked = require('marked');
console.log(marked('I am using __markdown__.'));
// Outputs: <p>I am using <strong>markdown</strong>.</p>
```

For further usage instructions, please see the original marked [documentation](https://github.com/chjj/marked).

Marked-for-chat excludes parsing for headings, blockquotes, and horizatonals. Parsing for breaks and tables can be excluded by setting options.

```js
marked.setOptions({
  renderer: new marked.Renderer(),
  gfm: true,
  tables: false,
  breaks: false,
}); 
```
Includes parsing for youtube videos `[![video]()](https://www.youtube.com/watch?v=video_id)`.

```js
var marked = require("marked-for-chat")
console.log(marked('[![video]()](https://www.youtube.com/watch?v=video_id)'))
// Outputs: "<p><iframe src="http://www.youtube.com/embed/video_id"></p> 
```

[marked](https://github.com/chjj/marked)
[gfm](https://help.github.com/articles/github-flavored-markdown)
[gfmf](http://github.github.com/github-flavored-markdown/)
