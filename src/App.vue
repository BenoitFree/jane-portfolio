<template>
  <div v-if="!isMobile()" id="app">
    <Header/>
    <router-view/>
    <Footer/>
  </div>
  <div v-else id="app">
    <Mobile/>
  </div>
</template>

<script>
import Header from '@/components/partials/header.vue'
import Footer from '@/components/partials/footer.vue'
import Mobile from '@/components/mobile.vue'
export default {
  components: {
    Header,
    Footer,
    Mobile
  },
  methods: {
    isMobile() {
      if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true
      } else {
        return false
      }
    }
  },
}
</script>