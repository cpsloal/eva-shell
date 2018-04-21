<!--
  @TAG:APPLAYOUT:LANDINGPAGE
  This component implements a default component to show when the app loads
-->

<template>
  <section class="hero is-fullheight Vue-LandingPage">
    <div class="hero-body">
      <section class="level">
        <div class="column is-narrow">
          <img class="" src="~@/assets/eva.logo.256x256.png" alt="eva-shell">
        </div>
        <div class="column doc">
          <h1 class="title is-3">Welcome to your new Eva-shell project!</h1>
          <p><a @click="open('https://github.com/cpsloal/eva-shell')">Eva-shell</a> comes packed with details on the changes made from <a @click="open('https://simulatedgreg.gitbooks.io/electron-vue/content/')">electron-vue</a> to become this application shell that you can use to build your application.</p>
          <button class="button is-primary is-rounded" @click="open('https://github.com/cpsloal/eva-shell')">Read the Eva-shell Docs</button>
          <div class="container">
            <h2 class="subtitle">Other Documentation</h2>
            <ul>
              <li><a class="alt" @click="open('https://simulatedgreg.gitbooks.io/electron-vue/content/')">Electron-Vue</a></li>
              <li><a class="alt" @click="open('https://electron.atom.io/docs/')">Electron</a></li>
              <li><a class="alt" @click="open('https://vuejs.org/v2/guide/')">Vue.js</a></li>
              <li><a class="alt" @click="open('https://bulma.io/')">Bulma.io</a></li>
            </ul>
          </div>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'landing-page',
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style scoped>
  .doc {
    padding-left: 60px;
    max-width: 700px;
  }

  .doc button {
    margin: 20px 0px;
  }
  
  .doc .subtitle {
    margin-bottom: 0px;
  }
</style>
