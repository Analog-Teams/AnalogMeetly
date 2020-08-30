<template>
  <div class="app">
    <div class="container-fliud">
      <div class="row">
        <div class="col-12" >
          <Home />
          <Meetings @queryString="queryData"/>
          <Lists :meetings="meetingList"/>
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
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
      meetingList: []
    }
  },
  methods: {
    queryData(){
      axios.get('https://my-json-server.typicode.com/ZachyDev/ZachyAPI/companies')
        .then(res => {
          console.log(res.data);
          this.meetingList = res.data
        })
        .catch(err => {
          console.log(err)
        })
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