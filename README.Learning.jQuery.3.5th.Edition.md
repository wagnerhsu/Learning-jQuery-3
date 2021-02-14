
## 01 Getting Started
- bane
- riddance 

## 02 Selecting Elements
- `:eq(1)` selects the second item in the set because JavaScript array numbering is zero-based, meaning that it starts with zero. In contrast, CSS is one-based, so a CSS selector such as `$('div:nth-child(1)')` would select all div selectors that are the first child of their parent
> :bulb: `:nth-child()` is the only jQuery selector that is one based
- It's important to note that the :contains() selector is case sensitive. It's also important to note that :contains() can cause catastrophically bad performance
- The `.filter()` method in particular has enormous power because it can take a function as its argument
- To access the first DOM element referred to by a jQuery object, for example, we would use `.get(0)`

## 03 Handling Events
- The `window.onload` event fires when a document is completely downloaded to the browser. On the other hand, a handler registered using `$(() => {})` is invoked when the DOM is completely ready for use
- Using `$(() => {})` is almost always preferred over using an onload handler, but we need to keep in mind that, because supporting files may not have loaded, attributes such as image height and width are not necessarily available at this time. If these are needed, we may at times also choose to implement an `onload` handler; the two mechanisms can coexist peacefully.
- When we assign a function as a handler, we use the function name but omit the trailing parentheses. With the parentheses, the function is called immediately; without the parantheses, the name simply identifies, or references, the function, and can be used to call it later.
- When any event handler is triggered, the keyword this refers to the DOM element to which the behavior was attached.