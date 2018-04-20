<template>
  <div id="wrapper">
    <main>
      <div class="left-side">
        <img id="logo" src="~@/assets/eva.logo.256x256.png" alt="eva-shell">
      </div>

      <div class="right-side">
        <div class="title">
          Welcome to your new Eva-shell project!
        </div>
        <div class="doc">
          <p>
            <a @click="open('https://github.com/cpsloal/eva-shell')">Eva-shell</a> comes packed with details on the changes made from <a @click="open('https://simulatedgreg.gitbooks.io/electron-vue/content/')">electron-vue</a>
            to become this application shell that you can use to build your application.
          </p>
          <button @click="open('https://github.com/cpsloal/eva-shell')">Read the Eva-shell Docs</button><br><br>
        </div>
        <div class="doc">
          <div class="title alt">Other Documentation</div>
          <ul>
            <li>
              <a class="alt" @click="open('https://simulatedgreg.gitbooks.io/electron-vue/content/')">Electron-Vue</a>    
            </li>
            <li>
              <a class="alt" @click="open('https://electron.atom.io/docs/')">Electron</a>
            </li>
            <li>
              <a class="alt" @click="open('https://vuejs.org/v2/guide/')">Vue.js</a>
            </li>
            <li>
              <a class="alt" @click="open('https://bulma.io/')">Bulma.io</a>
            </li>
          </ul>
        </div>
      </div>
    </main>
  </div>
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

<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 60px 80px;
    width: 100vw;
  }

  #logo {
    height: auto;
    margin-bottom: 20px;
    width: 256px;
  }

  main {
    display: flex;
    justify-content: space-between;
  }

  main > div { flex-basis: 50%; }

  .left-side {
    display: flex;
    flex-direction: column;
  }

  .welcome {
    color: #555;
    font-size: 23px;
    margin-bottom: 10px;
  }

  .title {
    color: #2c3e50;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 6px;
  }

  .title.alt {
    font-size: 18px;
    margin-bottom: 10px;
  }

  .doc p {
    color: black;
    margin-bottom: 10px;
  }

  .doc button {
    font-size: .8em;
    cursor: pointer;
    outline: none;
    padding: 0.75em 2em;
    border-radius: 2em;
    display: inline-block;
    color: #fff;
    background-color: #4fc08d;
    transition: all 0.15s ease;
    box-sizing: border-box;
    border: 1px solid #4fc08d;
  }

  .doc a.alt {
    color: #42b983;
    background-color: transparent;
  }

  .doc ul {
    list-style: none;
  }
</style>
