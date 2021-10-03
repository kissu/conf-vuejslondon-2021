<h3 class="!text-green-500 text-sm">1. Do not mutate vuex store state outside mutation handlers</h3>

<v-clicks>

- [Vuex strict mode](https://vuex.vuejs.org/guide/forms.html#two-way-computed-property)
- Enabled by default [in Nuxt](https://nuxtjs.org/docs/directory-structure/store#vuex-strict-mode)
- you can use `export const strict = false` to disable it in `/store/index.js`

</v-clicks>

<v-click>

Be careful of shallow copy ([good answer](https://stackoverflow.com/a/69323208/8816585) explaining this)
```js
const items = [...arr] ❌ this is a shallow copy
const items = JSON.parse(JSON.stringify(arr)) ✅ this is a proper deep copy!
```

</v-click>

<v-click>

Even better solution (because of this [possible issue](https://flaviocopes.com/how-to-clone-javascript-object/#json-serialization) mainly)

```html {2|6|all}
<script>
import { cloneDeep } from 'lodash-es'

export default {
  ...
  const deeplyClonedArray = cloneDeep(this.deeplyNestedArray)
}
</script>
```

</v-click>
