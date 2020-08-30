<template>
  <div class="app">
    <div class="container-fliud">
      <div class="row">
        <div class="col-12" >
          <Home />
          <Meetings />
          <Lists />
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
import Lists from './components/Lists';
export default {
  components: {
    Home,
    Meetings,
    Footer,
    Lists
  },
  data() {
    return{
      
    }
  }
}
</script>

<style scoped>
  .app{
    max-width: 100%;
    overflow: hidden;
  }
</style>