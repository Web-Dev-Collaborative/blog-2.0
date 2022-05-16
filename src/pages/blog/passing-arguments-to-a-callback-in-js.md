---
title: Passing Arguments To A Callback In JS
template: post
subtitle: By default you cannot pass arguments to a callback function
excerpt: By default you cannot pass arguments to a callback function
date: 2022-04-17T08:07:40.104Z
image: call-stack-first-example.png
thumb_image: call-stack-first-example.png
image_position: top
author: src/data/authors/bgoon.yaml
categories:
  - src/data/categories/js.yaml
tags:
  - src/data/tags/ds-algo.yaml
show_author_bio: true
related_posts:
  - src/pages/blog/data-structures-algorithms-resources.md
cmseditable: true
---
By default you cannot pass arguments to a callback function. For example:

```js
function callback() {
    console.log('Hi human');
}

document.getElementById('someelem').addEventListener('click', callback);
```

You can take advantage of the closure scope in Javascript to pass arguments to callback functions. Check this example:

```js
function callback(a, b) {
    return function () {
        console.log('sum = ', a + b);
    };
}

var x = 1,
    y = 2;
document.getElementById('someelem').addEventListener('click', callback(x, y));
```

### What are closures?

Closures are functions that refer to independent (free) variables. In other words, the function defined in the closure 'remembers' the environment in which it was created. [Check MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures) to learn more.

So this way the arguments `x` and `y` are in scope of the callback function when it is called.

Another method to do this is using the `bind` method. For example:

```js
var alertText = function (text) {
  alert(text);
};

document
  .getElementById("someelem")
  .addEventListener("click", alertText.bind(this, "hello"));
```
