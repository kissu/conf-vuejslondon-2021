<h3 class="!text-green-500 text-sm">3. Either my window/document or navigator is undefined</h3>

<v-clicks>

- Nuxt is a Vue app + SSR (if `ssr: true` in `nuxt.config.js`)
- Be aware that your code runs both on browser and on server
- eg: `window` is not defined on the server

</v-clicks>

<v-click>

Some ways to solve this

```js
plugins: [{ src: '@/plugins/calendly.js', mode: 'client' }]
```

</v-click>

<v-click>

```js
if (process.browser){
  console.log("my window's width on the client is >>", window.innerWidth)
}
```

</v-click>

<v-click>

Import it only when needed thanks to [dynamic imports in Nuxt](https://stackoverflow.com/a/67825061/8816585)

```js
async mounted() {
  if (process.browser) {
    const Ace = await import('ace-builds/src-noconflict/ace')
    Ace.edit...
  }
},
```

</v-click>
