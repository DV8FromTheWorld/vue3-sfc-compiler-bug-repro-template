<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <br />Demo code starts in the App.vue file.
    <br />If there is something to display it will appear here.

    <ErrorBoundary>
      <!-- Put testing code in here if required -->
    </ErrorBoundary>
  </div>
</template>

<script>
  import ErrorBoundary from './components/ErrorBoundary'

  export default {
    name: 'App',
    components: {
      ErrorBoundary,
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
