<template>
  <div class="meetings">
      <!-- add meeting notes -->
      <div class="add-notes">
          <h1>Add Meeting Notes</h1>
          <div class="form">
              <input type="text" class="form-control" placeholder="Type of meeting" v-model="type">
              <input type="text" class="form-control" placeholder="Name of department" v-model="department">
              <input type="date" class="form-control" placeholder="Date of meeting" v-model="date">
              <input type="number" class="form-control" placeholder="Number of attendants" v-model="attendees">
              <button type="button" @click="saveNotes">Add Note(s)</button>
          </div>
      </div>
      <!-- search meeting -->
      <div class="search-meetings">
          <h1>Search Meeting</h1>
          <div class="form">
              <input type="text" class="form-control" placeholder="Filter by meeting type" v-model="fmType">
              <input type="text" class="form-control" placeholder="Filter by department name" v-model="fmDepartment">
              <input type="date" class="form-control" placeholder="Filter by date" v-model="fmDate">
              <input type="number" class="form-control" placeholder="Filter by attendants" v-model="fmAttendees">
              <button type="button" @click="filterMeetingsData">Filter Meeting(s)</button>
          </div>
      </div>
      <!-- search notes -->
      <div class="search-notes">
          <h1>Search Notes</h1>
          <div class="form">
              <input type="text" class="form-control" placeholder="Filter by meeting type" v-model="fnType">
              <input type="text" class="form-control" placeholder="Filter by department name" v-model="fnDepartment">
              <input type="date" class="form-control" placeholder="Filter by date" v-model="fnDate">
              <input type="number" class="form-control" placeholder="Filter by attendants" v-model="fnAttendees">
              <button type="button" @click="filterNotesData">Filter Note(s)</button>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "Meetings",
    data() {
        return{
            type: '',
            department: '',
            date: '',
            attendees: '',
            fnType: '',
            fnDepartment: '',
            fnDate: '',
            fnAttendees: '',
            fmType: '',
            fmDepartment: '',
            fmDate: '',
            fmAttendees: ''
        }
    },
    methods: {
       saveNotes() {
        this.$emit('saveNotes',this.type,this.date,this.department,this.attendees);
        alert('A new record has been added')
       },
      //filterMeetingsData
      filterMeetingsData() {
          this.$emit('filterMeetingsData',this.fmType,this.fmDate,this.fmDepartment,this.fmAttendees);
      },
       //filterNotessData
      filterNotesData() {
          this.$emit('filterNotesData',this.fnType,this.fnDate,this.fnDepartment,this.fnAttendees);
      }

    }
}
</script>

<style scoped>
@media (min-width:768px) {
    
    .meetings{
        width: 100%;
        max-width: 100%;
        background: rgba(0,0,0,1);
        height: 60vh;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
    }
    .meetings h1{
        color: #fff;
        font-family: 'Baloo Tamma 2', cursive;
        font-size: 40px;
    }
    .meetings input{
        margin-top:15px;
        padding: 20px;
        max-width: 450px;
        margin-left: 13px;
    }
    .add-notes{
        margin:40px 20px;
    }
    .search-meetings{
        margin: 40px 20px;
    }
    .search-notes{
        margin:40px 20px; 
    }
    .meetings button {
        padding: 15px;
        width: 200px;
        max-width: 200px;
        margin: 20px 12px;
        background: #6613ED;
        border:none;
        outline: none;
        color: #fff;
        font-family: 'Poppins',san-serif;
        font-size: 15px;
    }
    .meetings button:hover{
        background: #7e49d3;
        transition: 200ms ease-out;
    }
}
    @media (max-width:768px) {
        .meetings {
            max-height: 100%;
            height: 30%;
            display: block;
            width: 100%;
            max-width: 100%;
            background: rgba(0,0,0,1);
        }
        .meetings h1{
            color: #fff;
            font-family: 'Baloo Tamma 2', cursive;
            font-size: 30px;
        }
        .meetings input {
            margin-top:15px;
            padding: 20px;
            max-width: 450px;
      
        }
        .meetings .search-meetings {
            margin:40px;
        }
        .meetings .add-notes {
            margin: 40px;
        }
        .meetings .search-notes{
            margin:40px;
        }
         .meetings button {
            padding: 15px;
            width: 200px;
            max-width: 200px;
            margin: 20px 2px;
            background: #6613ED;
            border:none;
            outline: none;
            color: #fff;
            font-family: 'Poppins',san-serif;
            font-size: 15px;
            cursor: pointer;
        }
        .meetings button:hover{
            background: #8860c9;
            transform: scale(0.9);
            transition: 200ms ease-in;
        }
    }
  
</style>