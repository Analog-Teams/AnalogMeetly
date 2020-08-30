<template>
  <div class="meetings">
      <!-- add meeting notes -->
      <div class="add-notes">
          <h1>Add Meeting Notes</h1>
          <div class="form">
              <input type="text" class="form-control" placeholder="Type of meeting">
              <input type="text" class="form-control" placeholder="Name of department">
              <input type="date" class="form-control" placeholder="Date of meeting">
              <input type="number" class="form-control" placeholder="Number of attendants">
              <button type="button">Add Note(s)</button>
          </div>
      </div>
      <!-- search meeting -->
      <div class="search-meetings">
          <h1>Search Meeting</h1>
          <div class="form">
              <input type="text" class="form-control" placeholder="Filter by meeting type">
              <input type="date" class="form-control" placeholder="Filter by department name">
              <input type="date" class="form-control" placeholder="Filter by date">
              <input type="number" class="form-control" placeholder="Filter by attendants">
              <button type="button">Filter Meeting(s)</button>
          </div>
      </div>
      <!-- search notes -->
      <div class="search-notes">
          <h1>Search Notes</h1>
          <div class="form">
              <input type="text" class="form-control" placeholder="Filter by meeting type">
              <input type="date" class="form-control" placeholder="Filter by department name">
              <input type="date" class="form-control" placeholder="Filter by date">
              <input type="number" class="form-control" placeholder="Filter by attendants">
              <button type="button">Filter Note(s)</button>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "Meetings"
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