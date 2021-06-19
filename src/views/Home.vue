<template>
<div id="swiper-home" class="swiper-projets swiper-container">
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
import image_camus from "@/assets/img/projets/Camus.png"
import image_doort from "@/assets/img/projets/Doort.png"
import image_metapoly from "@/assets/img/projets/Metapoly.png"
import image_mira from "@/assets/img/projets/Mira.png"
import separator from "@/assets/img/separator.png"
import arrowPrev from "@/assets/img/arrow-prev.png"
import arrowNext from "@/assets/img/arrow-next.png"
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

const initSwiperHome = () => {
    // Init Swiper
    let swiper = new Swiper("#swiper-home", {
        // Optional parameters
        loop: true,
        effect: "fade",
        direction: "vertical",
        mousewheel: true,
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
            title: "UI/UX DESIGN",
            description: "E-shop - METAPOLY",
            lien: "https://metapoly.fr",
            image: image_metapoly,
            color_background: "#E8DBD8",
          },
        },
        {
          projet: {
            title: "PRINT DESIGN",
            description: "Print design - Retail stand Camus",
            lien: "test",
            image: image_camus,
            color_background: "#C6BCB5",
          },
        },
        {
          projet: {
            title: "Global Design",
            description: "Global design - Product launch Doort",
            lien: "test",
            image: image_doort,
            color_background: "#6A6983",
          },
        },
        {
          projet: {
            title: "UI/UX DESIGN",
            description: "E-commerce - MIRA",
            lien: "https://boutiquemira.fr",
            image: image_mira,
            color_background: "#79C1A8"
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
  left: 4rem;
  top: 29rem;
}
body.home .swiper-button-prev{
  background-image: url("../assets/img/arrow-prev.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
  left: 4rem;
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
  left: 4rem;
  top: 29rem;
}
body.home .swiper-button-prev{
  background-image: asset("arrow-prev.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
  left: 4rem;
  top: 24rem;
}
</style>
<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';
@media screen and(min-width: 1000px) and (max-width: 1445px) {
  .home{
    & h2.titre{
      font-size: 160px !important;
    }
    & h3.description{
      font-size: 25px !important;
    }
    & .following button{
      width: 310px!important;
      font-size: 25px !important;
      height: 60px!important;
    }
    .slide-right img{
      width: 310px !important;
    }
  }
}

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
      font-size: 202px;
      text-transform: uppercase;
      color: #fff;
      line-height: .8;
      margin: 0;
      max-width: 200px;
      padding-top: 12px;
    }
    & h3{
      font-family: 'Oswald', sans-serif !important;
      font-size: 30px;
      font-weight: 200;
      color: #fff;
    }
    & .slide-right img{
      width: 350px;
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
        width: 350px;
        height: 70px;
      }
    }
  }

  & .slide-left img {
    display: block;
    width: 528px;
    height: 528px;
  }

  & .slide-svg{
    position: absolute;
    right: 0;
    bottom: 0;
    z-index: 0;
    height: auto;
    width: auto;
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

  $breakpoint-laptop: 1605px;
  $breakpoint-macbook: 1445px;
  $breakpoint-ipadpro: 1055px;
  $breakpoint-tablet: 768px;
  @media (min-width: $breakpoint-tablet) and (max-width: $breakpoint-laptop) {
    .slide-left img {
      display: block;
      width: 428px;
      height: 428px;
      object-fit: cover;
    }
    .slide-svg{
      right: -3rem;
      height: 110%;
    }
  }
}
</style>