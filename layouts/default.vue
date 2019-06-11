<template>
  <div>
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  font-family: 'M PLUS 1p', sans-serif;
  margin: 0;
  padding: 0;
}

</style>
