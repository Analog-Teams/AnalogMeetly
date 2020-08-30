<template>
  <div class="footer">
      <div class="logo">
          <img :src="require(`@/assets/${'flogo.png'}`)" alt="analogmeetly">
      </div>
      <div class="location">
          <h2>Ghana,kenya</h2>
      </div>
  </div>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped>
    .footer{
        background: #fff;
        max-width: 100%;
        height:20vh;
        width: 100%;
        margin:30px 20px;
    }
</style>