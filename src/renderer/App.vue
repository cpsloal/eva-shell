<template>
  <div id="app" class="Vue-App">
    <app-main></app-main>
  </div>
</template>

<script>
  // @TAG:APPLAYOUT:IMPORT
  // Import Vue components that make up the application layout
  import { AppMain } from './components/layout/'

  export default {
    name: 'eva-shell',
    components: {
      AppMain
    }
  }
</script>

<style lang="scss">
  /* SCSS */
  // @TAG:APPLAYOUT:STYLING
  // Bulma CSS is loaded in /src/renderer/assets/globals.scss
</style>
