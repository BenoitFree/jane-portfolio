<template>
  <div id="app">
    <Header/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/partials/header.vue'
import Footer from '@/components/partials/footer.vue'
export default {
  name: 'Home',
  components: {
    Header,
    Footer
  }
}
</script>