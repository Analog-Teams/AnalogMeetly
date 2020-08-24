<template>
  <div class="app">
    <div class="container-fliud">
      <div class="row">
        <div class="col-12" >
          <!-- Login component -->
          <Login />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Login from './components/Login';
export default {
  components: {
    Login

  }
}
</script>

<style scoped>
  .app{
    max-width: 100%;
    overflow: hidden;
  }
</style>