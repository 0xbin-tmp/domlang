<!--<p align="center">-->
<!--  <a href="https://getbootstrap.com/">-->
<!--    <img src="https://getbootstrap.com/docs/4.3/assets/brand/bootstrap-solid.svg" alt="Bootstrap logo" width="72" height="72">-->
<!--  </a>-->
<!--</p>-->

<h3 align="center">DOMLang JS</h3>

<p align="center">
  A light-weight JavaScript library to building web app easier.
  <br>
  <a href="https://getbootstrap.com/docs/4.3/"><strong>Explore domlang docs »</strong></a>
  <br>
  <br>
  <a href="https://github.com/twbs/bootstrap/issues/new?template=bug.md">Report bug</a>
  ·
  <a href="https://github.com/twbs/bootstrap/issues/new?template=feature.md&labels=feature">Request feature</a>
</p>

<p align="center">
  [![Build Status](https://travis-ci.org/0xWiz/domlang.svg?branch=master)](https://travis-ci.org/0xWiz/domlang)
  [![License](https://img.shields.io/github/license/0xWiz/domlang.svg)](https://github.com/0xWiz/Fraction/blob/master/LICENSE)
  [![Version](https://img.shields.io/github/release/0xWiz/domlang.svg)](https://github.com/0xWiz/Fraction/releases/latest)
</p>


## Quick start

Clone the github repo `git clone https://github.com/0xWiz/domlang.git` and under the `dest` folder, you can find the minified version of the `domalang`

Add it to your HTML as you would add any JavaScript files.

## DOM methods

- [$(selector)](#dom-method-$)
- [.append(\[arugments\])](#dom-method-append)
- [.attr(key, \[value\])](#dom-method-attr) or [.prop(key, \[value\])](#dom-method-attr)
- [.bind(event, callback)](#dom-method-bind)
- [.children(\[includeTextNodes=false\])](#dom-method-children)


<h3 id="dom-method-$">$(selector)</h3>

Allows you to create a new `domlang` instance, you can pass the following as argument.

- `String`      — If it is an HTML string then it will create those element and add it to the current instance, or it will select elements from the DOM itself.
- `HTMLElement` — Add the given HTMLElement to the current instance.
- `Array`       — Add all the elements from the array to the current instance if the element is a HTMLElement.

**Example →**

```js
let buttons = $("button"); 
```


<h3 id="dom-method-append">.append([arguments])</h3>

Append HTML element(s) to the selected elements. You can pass the following as argument.

- `String`      — Select element(s) from the DOM and append them to the selected elements.
- `HTMLElement` — Append given HTMLElement to the selected elements.
- `Array`       — Append all the elements from given array to the selected elements if the array element is a HTML element.
- `arguments`   — You can pass all above parameters as arguments. Example : `$("#container").append(element1, element2)`

**Example →**

```js
let span = $("<span>+</span>");
$("ul li").append(span);
```

<h3 id="dom-method-attr">.attr(key, [value])</h3>

Get or set HTML element(s) attribute. :warning: If key only passed as argument, it will return the first element's attribute.

**Example →**

```js
$("a").attr("href", "not-found.html");

let action = $("form").attr("action");
```


<h3 id="dom-method-bind">.bind(event, callback)</h3>

Bind an event listener to selected element(s). :information_source: It is a wrapper around `addEventListener` method.

**Example →**

```js
$("button").bind("click", function() {
    alert(this.text());
});
```

<h3 id="dom-method-children">.children([includeTextNodes=false])</h3>

Get all the children of the first element from the selected elements. Pass `true` as argument to include all the `text` nodes.

**Example →**

```js
$("ul").children().each(function(i) {
  this.text(this.text() + " " + i);
});
```

