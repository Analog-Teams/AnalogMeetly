<template>
  <div class="lists">
      <table class="table" v-if="meetings.length>0">
  <thead class="thead-dark">
    <tr>
      <th scope="col">Date</th>
      <th scope="col">Type of meeting</th>
      <th scope="col">Department</th>
      <th scope="col">Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr :key="meeting.date" v-for="meeting in meetings">
      <td>{{meeting.date}}</td>
      <td>{{meeting.type}}</td>
      <td>{{meeting.department}}</td>
      <td> <a href="http://my-json-server.typicode.com/ZachyDev/meetlydb/meetings?notes/1" target="_blank">Read</a></td>
      
    </tr>
  </tbody>
</table>
  </div>
</template>

<script>
export default {
    name: "Lists",
    props: ["notes","meetings"]
}
</script>

<style>

</style>