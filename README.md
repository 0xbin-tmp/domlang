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

## Quick start

Clone the github repo `git clone https://github.com/0xWiz/domlang.git` and under the `dest` folder, you can find the minified version of the `domalang`

Add it to your HTML as you would add any JavaScript files.

[![Build Status](https://travis-ci.org/0xWiz/domlang.svg?branch=master)](https://travis-ci.org/0xWiz/domlang)
[![License](https://img.shields.io/github/license/0xWiz/domlang.svg)](https://github.com/0xWiz/domlang/blob/master/LICENSE)
[![Version](https://img.shields.io/github/release/0xWiz/domlang.svg)](https://github.com/0xWiz/domlang/releases/latest)


## DOM methods

- [$(selector)](#dom-method-$)
- [.append(\[arugments\])](#dom-method-append)
- [.also(callback)](#dom-method-also)
- [.attr(key, \[value\])](#dom-method-attr) or [.prop(key, \[value\])](#dom-method-attr)
- [.bind(event, callback)](#dom-method-bind)
- [.children(\[includeTextNodes=false\])](#dom-method-children)
- [.clear()](#dom-method-clear)
- [.click(callback)](#dom-method-click)
- [.css(key, \[value\])](#dom-method-css)
- [.disable()](#dom-method-disable)
- [.enable()](#dom-method-enable)
- [.extend(\[arguments\])](#dom-method-extend)
- [.isDisabled()](#dom-method-isDisabled)


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

<h3 id="dom-method-append">.also(callback)</h3>

This is method is an utility method. The first selected element will be set to the callback for further processing, and this method will return whatever elements was before this method called.

**Example →**

```js
$("input[type='username']").also(function() {
  if (this.isDisabled()) {
    this.enable();
  }
});
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

<h3 id="dom-method-clear">.clear()</h3>

Clear all events of selected elements.

**Example →**

```js
let buttons = $("button").bind("click", function() {
  alert("hello");
});

buttons.clear();
```

<h3 id="dom-method-click">.click(callback)</h3>

Bind a click event to selected elements.

**Example →**

```js
$("button").click(function() {
  alert(this.text());
});
```


<h3 id="dom-method-css">.css(key, [value])</h3>

Add CSS style to selected elements. You can pass the following as first argument.

- `String` — pass the CSS style property as the key and pass the CSS style property value as second argument.
- `Object` — pass a JavaScript object as the first argument with all the CSS styles as key-value pair.

**Example →**

```js
let anchors = $("a");
anchors.css("color", "green");
anchors.css({
  textStyle: "none",
  display: "inline-block",
  padding: "5px"
});
```


<h3 id="dom-method-disable">.disable()</h3>

Disable selected form elements.

**Example →**

```js
$("input[type='username']").disable();
```


<h3 id="dom-method-enable">.enable()</h3>

Enable selected form elements.

**Example →**

```js
$("input[type='username']").enable();
```


<!--<h3 id="dom-method-extend">.extend([arguments])</h3>-->

<!--Allows you to add more elements to the current instance.. You can pass the following as first argument.-->

<!--- `String` — pass the CSS style property as the key and pass the CSS style property value as second argument.-->
<!--- `Object` — pass a JavaScript object as the first argument with all the CSS styles as key-value pair.-->

<!--**Example →**-->

<!--```js-->
<!--let anchors = $("a");-->
<!--anchors.css("color", "green");-->
<!--anchors.css({-->
<!--  textStyle: "none",-->
<!--  display: "inline-block",-->
<!--  padding: "5px"-->
<!--});-->
<!--```-->


<h3 id="dom-method-isDisabled">.isDisabled()</h3>

Check if the first element from selected elements is isDisabled or not.

**Example →**

```js
$("input[type='username']").also(function() {
  if (this.isDisabled()) {
    this.enable();
  }
});
```
