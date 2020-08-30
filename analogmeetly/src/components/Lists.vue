<template>
  <div class="lists">
      <table class="table">
  <thead class="thead-dark">
    <tr>
      <th scope="col">#</th>
      <th scope="col">Date</th>
      <th scope="col">Type of meeting</th>
      <th scope="col">Department</th>
      <th scope="col">Attendees</th>
    </tr>
  </thead>
  <tbody>
    <tr :key="meeting.id" v-for="meeting in meetings">
      <th scope="row">1</th>
      <td>{{meeting.id}}</td>
      <td>{{meeting.name}}</td>
      <td>{{meeting.location}}</td>
      <td>{{meeting.name}}</td>
    </tr>
  </tbody>
</table>
  </div>
</template>

<script>
export default {
    name: "Lists",
    props: ["meetings"]
}
</script>

<style>

</style>