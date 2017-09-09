# cc-template

### a nice template which deserve your notice !
### it is an Embedded JavaScript templates.

## Features

  * custom define the scope name `options.scope = 'theNameILike'`
  * custom define the regexpHead and the regexpTail `options.regexpHead = '{{'`
  * Unbuffered code for conditionals etc `<% code %>`
  * Escapes html by default with `<%= code %>`
  * Unescaped buffering with `<%- code %>`
  * dangerously insert data with `<%! code %>`

## Example

    <% if (scope.user) { %>
	    <h2><%= scope.user.name %></h2>
    <% } %>

## Try out a live example now

## Usage

    var compiled = new cc.Template().compile(str);
    // => Function

    compiled(data);
    // => str

## Options
  - `scope`       The scope name within the template string, defaulting to "scope"
  - `regexpHead`  Open tag, defaulting to "<%"
  - `regexpTail`  Closing tag, defaulting to "%>"

## Custom delimiters

Custom delimiters can also be applied globally:

    var template = new cc.Template({
      scope: 'it',
      regexpHead: '{{',
      regexpTail: '}}'
    });

Which would make the following a valid template:

    <h1>{{= it.title }}</h1>

## License

(The MIT License)

Copyright (c) 2017-2099 CongCong

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
