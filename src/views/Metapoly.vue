<template>
    <div>
        <h1>TEST</h1>
    </div>
</template>


<script>
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

export default {
  name: 'Metapoly',
  beforeCreate: function() {
    document.body.className = 'metapoly';
  }
}
</script>
<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';

</style>