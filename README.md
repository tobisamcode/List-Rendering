# List-Rendering
100 Days of Vue(List Rendering)

Mapping an Array to Elements with v-for

We can use the v-for directive to render a list of items based on an array. The v-for directive requires a special syntax in the form of item in items, where items is the source data array and item is an alias for the array element being iterated on:


Inside v-for blocks we have full access to parent scope properties. v-for also supports an optional second argument for the index of the current item.
You can also use of as the delimiter instead of in, so that it is closer to JavaScript’s syntax for iterators:
You can also use v-for to iterate through the properties of an object.

# Maintainance state
When Vue is updating a list of elements rendered with v-for, by default it uses an “in-place patch” strategy. If the order of the data items has changed, instead of moving the DOM elements to match the order of the items, Vue will patch each element in-place and make sure it reflects what should be rendered at that particular index. This is similar to the behavior of track-by="$index" in Vue 1.x.

This default mode is efficient, but only suitable when your list render output does not rely on child component state or temporary DOM state (e.g. form input values).

To give Vue a hint so that it can track each node’s identity, and thus reuse and reorder existing elements, you need to provide a unique key attribute for each item:
```html
<div v-for="item in items" v-bind:key="item.id">
  <!-- content -->
</div>
```

It is recommended to provide a key attribute with v-for whenever possible, unless the iterated DOM content is simple, or you are intentionally relying on the default behavior for performance gains.


# Technology

* HTML
* CSS
* JavaScript

* ![picture](https://github.com/tobisamcode/List-Rendering/blob/main/vuelist.jpg)
* ![picture](https://github.com/tobisamcode/List-Rendering/blob/main/vuelist2.jpg)
