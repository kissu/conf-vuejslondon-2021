---
preload: false
---

<h1 class="!text-green-500">Hi! 🍉</h1>

<h3>Konstantin BIFERT ~ <span
    class="text-transparent bg-clip-text bg-gradient-to-br from-orange-300 to-teal-700">kissu</span></h3>

<div class="flex mt-6">
  <img v-motion :initial="{ x: 30, y: -50, scale: 1, rotate: -200 }" :enter="final"
    class="top-0 left-0 right-0 bottom-0 h-24 w-24 rounded" src="/images/kissu.jpg"
    alt="photo of konstantin" />
  <section class="ml-4">
  <v-clicks>
    <p class="!m-0">
      🎨 Frontend Developer <a href="https://twitter.com/passionpeopleNL">@passionpeopleNL</a>
    </p>
    <p class="!my-2">
      <img src="/images/nuxt_logo.svg" class="inline h-6">
      <a href="https://nuxtjs.org/teams" class="ml-2">Nuxt.js Ambassador</a>
    </p>
    <p class="!my-2">
      <logos-stackoverflow-icon class="inline mr-2" />
      <a href="https://stackoverflow.com/users/8816585/kissu">Daily helper on Stackoverflow</a>
    </p>
    </v-clicks>
  </section>
</div>

<div class="mt-4"></div>

<v-clicks>

- This talk will follow the one at [Nuxtnation](https://nuxtnation.com/)
- ...it is already on the dedicated website and will soon be availble on YouTube
- Since this is a shorter talk, we'll focus more on the common Vue issues (undiscussed @nuxtnation)

</v-clicks>

<script setup lang="ts">
  const final = {
    x: 0,
    y: 0,
    rotate: 0,
    scale: 1,
    transition: {
      type: 'spring',
      damping: 10,
      stiffness: 20,
      mass: 2
    }
  }
</script>

<!--
feel free to check the videos of the conference, it's free!
-->
