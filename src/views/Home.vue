<template>
<div class="swiper-projets swiper-container">
  <!-- Additional required wrapper -->
  <div class="swiper-wrapper">
    <!-- Slides -->
    <div class="swiper-slide" v-for="item in items" :key="item.projets">
      <div class="swiper-content">
        <div class="slide-left">
            <img :src="item.projet.image">
        </div>
        <div class="slide-right">
          <h2 class="titre">{{ item.projet.title }}</h2>
          <img alt="separateur ligne" :src="separator">
          <h3 class="description">{{ item.projet.description }}</h3>
          <a class="following" :href="`${item.projet.lien}`"><button>View Project</button></a>
        </div>
      </div>
      <svg class="slide-svg" xmlns="http://www.w3.org/2000/svg" width="1733.364" height="1104.322" viewBox="0 0 1733.364 1104.322">
        <path id="Tracé_1" data-name="Tracé 1" d="M1233.9-1.489C997.569,38.089,813.161,156.206,822.419,520.381c11.448,450.388-737.065,565.357-737.065,565.357H1818.718V.478S1470.238-41.067,1233.9-1.489Z" transform="translate(-85.354 18.583)" :fill="item.projet.color_background"/>
      </svg>
    </div>
  </div>

  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>

</div>
</template>


<script>
import image_spray from "@/assets/img/projets/spray.png"
import image_doort from "@/assets/img/projets/doort.png"
import separator from "@/assets/img/separator.png"
import arrowPrev from "@/assets/img/arrow-prev.png"
import arrowNext from "@/assets/img/arrow-next.png"
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

const initSwiperHome = () => {
    // Init Swiper
    let swiper = new Swiper(".swiper-container", {
        // Optional parameters
        effect: "fade",
        direction: "vertical",
        fadeEffect: {
          crossFade: true,
        },
        // Navigation arrows
        navigation: {
            nextEl: ".swiper-button-next",
            prevEl: ".swiper-button-prev",
        },
    });
};

export default {
  name: 'Home',
  beforeCreate: function() {
      document.body.className = 'home';
  },
  mounted() {
      initSwiperHome();
  },
  updated() {
      initSwiperHome();
  },
  data: function () {
    return {
      separator: separator,
      arrowprev: arrowPrev,
      arrownext: arrowNext,
      color_primary: "#3F4367",
      color_secondar: "#3F4367",
      items: [
        {
          projet: {
            title: "Print Design",
            description: "Stand en grande distribution - CAMUS",
            lien: "test",
            image: image_spray,
            color_background: "#c6bcb5"
          },
        }, 
        {
          projet: {
            title: "Global Design",
            description: "Lancement de produit - DOORT",
            lien: "test",
            image: image_doort,
            color_background: "#3F4367",
          },
        },
        {
          projet: {
            title: "Identity Design",
            description: "Lorem",
            lien: "test",
            image: image_spray,
            color_background: "#c6bcb5",
          },
        },
      ]
    }
  }
}
</script>

<style>
body.home .swiper-button-next{
  background-image: url("../assets/img/arrow-next.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
  left: 8rem;
  top: 29rem;
}
body.home .swiper-button-prev{
  background-image: url("../assets/img/arrow-prev.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
  left: 8rem;
  top: 24rem;
}
body.home .swiper-button-prev::after, .swiper-button-next::after{
  display: none !important;
}
body.home {
    position: relative !important;
    height: 100% !important;
    overflow: hidden !important;
    padding: 0 !important;
    margin: 0 !important;
}
@media (min-width: 1606px){
  body.home .swiper-button-prev{
    top: 30rem !important;
  }
  body.home .swiper-button-next{
    top: 35rem !important;
  }
}
</style>
<style lang="postcss" scoped>
@function asset($path) {
  @return url("~@/assets/#{$path}");
}
body.home .swiper-button-next{
  background-image: asset("arrow-next.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
  left: 8rem;
  top: 29rem;
}
body.home .swiper-button-prev{
  background-image: asset("arrow-prev.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
  left: 8rem;
  top: 24rem;
}
</style>
<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';

#app { height: 100% }
html {
  position: relative;
  height: 100%;
}
.swiper-container {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.swiper-projets{

  & .swiper-slide {
    position: relative;
    display: flex;
    height: 100%;
    justify-content: center;
  }

  & .swiper-content{
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    column-gap: 5rem;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
    padding-left: 10rem;
    width: 100%;
    & h2{
      font-family: "AméliaDisplay" !important;
      font-size: 260px;
      text-transform: uppercase;
      color: #fff;
      line-height: .8;
      margin: 0;
      max-width: 200px;
    }
    & h3{
      font-family: 'Oswald', sans-serif !important;
      font-size: 35px;
      font-weight: 200;
      color: #fff;
    }
    & .following{
      display: block;
      & :hover{
        background: rgba(209, 209, 209, 0.15);
      }
      & button{
        background-color:#FFFFFF;
        box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
        border: none;
        text-transform: uppercase;
        font-family: 'Oswald', sans-serif !important;
        font-size: 30px;
        font-weight: bold;
        cursor: pointer;
        transition: 0.25s ease;
        width: 397px;
        height: 70px;
      }
    }
  }

  & .slide-left img {
    display: block;
    width: 628px;
    height: 628px;
  }

  & .slide-svg{
    position: absolute;
    right: 0;
    bottom: 0;
    z-index: 0;
  }

  & .slide-left, .slide-right{
    position: relative;
    z-index: 22;
    flex: 1;
  }

  & .slide-left > img{
    margin-right: 0;
    margin-left: auto;
  }

  $breakpoint-tablet: 768px;
  $breakpoint-laptop: 1605px;
  @media (min-width: $breakpoint-tablet) and (max-width: $breakpoint-laptop) {
    .slide-left img {
      display: block;
      width: 428px;
      height: 428px;
      object-fit: cover;
    }
    .slide-svg{
      right: -15rem;
    }
  }
}
</style>