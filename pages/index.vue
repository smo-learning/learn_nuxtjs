<template>
  <section class="container">
    <div>{{ text }}</div>
  </section>
</template>

<script>
import axios from 'axios'
export default {
  asyncData(context) {
    return axios
      .get('https://corporatebs-generator.sameerkumar.website/')
      .then(res => {
        return { text: res.data.phrase }
      })
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
