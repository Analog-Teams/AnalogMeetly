<template>
  <div class="app">
    <div class="container-fliud">
      <div class="row">
        <div class="col-12" >
          <Home />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Home from './components/Home';
export default {
  components: {
    Home
  }
}
</script>

<style scoped>
  .app{
    max-width: 100%;
    overflow: hidden;
  }
</style>