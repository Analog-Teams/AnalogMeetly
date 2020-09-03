<template>
  <div class="app">
    <div class="container-fliud">
      <div class="row">
        <div class="col-12" >
          <Home />
          <Meetings @saveNotes="saveNotes" @filterMeetingsData="filterMeetingsData" @filterNotesData="filterNotesData"/>
          <Lists :notes="saveAllNotes" :meetings="filteredData"/>
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
      saveAllNotes: [],
      notesArray: [],
      filteredData: []
    }
  },
  methods: {
    saveNotes(type,date,department,attendees) {
      this.notesArray = {type,date,department,attendees};
      return this.saveAllNotes.push(this.notesArray);
    },
    filterMeetingsData(type,date,department,attendees) {
      console.log(type,date,department,attendees)
      axios.get(`http://my-json-server.typicode.com/ZachyDev/meetlydb/meetings?type=${type}`)
        .then(res=> {
          // console.log(res.data)
          this.filteredData = res.data;

        })
        .catch(err => console.log(err))
    },
    filterNotesData(type,date,department,attendees) {
      console.log(type,date,department,attendees);
       axios.get(`http://my-json-server.typicode.com/ZachyDev/meetlydb/meetings?type=${type}`)
        .then(res=> {
          // console.log(res.data)
          this.filteredData = res.data;

        })
        .catch(err => alert('Record not found!',err))
    },
    
  }

}
</script>

<style scoped>
  .app{
    max-width: 100%;
    overflow: hidden;
  }
</style>