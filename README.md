<p align="center">
  <img src="https://raw.githubusercontent.com/stephan281094/vue-drag-select/master/images/screenshot.png"
    alt="Screenshot">
</p>

# Vue Drag to Select Component
A Vue component for drag selecting elements. Inspired by [react-drag-select](https://github.com/pablofierro/react-drag-select).

## Demo
* Visit the demo [here](http://vue-drag-select-example.now.sh).

## Usage
* Add `vue-drag-select` to your project:

```bash
$ yarn add vue-drag-select # or npm i --save vue-drag-select
```

* Import the component and add it to your template:

```js
import DragSelect from 'vue-drag-select/src/DragSelect.vue'

export default {
  components: {
    'drag-select-container': DragSelect
  }
}
```

* Wrap the items that you want to be selectable in the `drag-select-container`
  with a `selectorClass` property and a scoped slot:
  
* You can optionally `useDoubleclick` prop, which might be helpful if you need also drag items. It works like doubleclick + mousedown

```vue
<template>
  <drag-select-container selectorClass="itemToBeSelected" useDoubleclick>
    <template slot-scope="{ selectedItems }">
      <!-- Your items here -->
    </template>
  </drag-select-container>
</template>
```

* Then write your own logic to make items look selected. For instance
  by applying a class.

## License
MIT
