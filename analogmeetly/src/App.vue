<template>
  <div class="app">
    <div class="container-fliud">
      <div class="row">
        <div class="col-12" >
          <Home />
          <Meetings />
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Home from './components/Home';
import Meetings from './components/Meetings';
import Footer from './components/Footer';
export default {
  components: {
    Home,
    Meetings,
    Footer
  }
}
</script>

<style scoped>
  .app{
    max-width: 100%;
    overflow: hidden;
  }
</style>