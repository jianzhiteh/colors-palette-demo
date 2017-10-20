<template>
  <div id="app">
    <nav class="navbar navbar-dark bg-primary">
        <div class="container">
            <a class="navbar-brand" href="#">Color Palettes</a>
        </div>
    </nav>
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app >.container {
  padding-top: 20px;
  padding-bottom: 20px;
}
</style>

