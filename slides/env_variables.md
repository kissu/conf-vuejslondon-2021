<h3 class="!text-green-500 text-sm">2. My code is not working on production</h3>

<v-clicks>

- Double check that this is working locally at first:
  - `yarn build` and `yarn start` if `target: 'server'` (default)
  - `yarn generate` and `yarn start` otherwise
- Check that your env variables are properly defined ([How to use .env variables in Nuxt?](https://stackoverflow.com/questions/67703133/how-to-use-env-variables-in-nuxt/67705541#67705541))
- Double check that those are defined on production (somewhere in your app build settings)
- Try to isolate your issue and reduce the amount of things that can mess things up
- Try to quickly host your app somewhere else for debugging purposes ([various integrations](https://nuxtjs.org/integrations) with Nuxt)

</v-clicks>
