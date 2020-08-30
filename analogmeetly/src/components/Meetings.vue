<template>
  <div class="meetings">
      <!-- add meeting notes -->
      <div class="add-notes">
          <h1>Add Meeting Notes</h1>
      </div>
      <!-- search meeting -->
      <div class="search-meeting">
          <h1>Search Meeting</h1>
      </div>
      <!-- search notes -->
      <div class="search-notes">
          <h1>Search Notes</h1>
      </div>
  </div>
</template>

<script>
export default {
    name: "Meetings"
}
</script>

<style scoped>
    .meetings{
        width: 100%;
        max-width: 100%;
        background: rgba(0,0,0,1);
        height: 60vh;
    }
</style>