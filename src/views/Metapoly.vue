<template>
    <div id="metapoly" class="scroll-container" data-scroll-container>
        <div class="scroll-section start" data-scroll-section>
            <div>
                <h1>E-shop - METAPOLY</h1>
                <p>
                    Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values. I worked on their e-commerce from a simple and modern style that leaves room for the beauty of the furniture in a sober and elegant way.
                    When creating an e-shop it is important to keep it simple. Your customer wants to go directly to your articles. For this the number of clicks is very important, there is every interest in reducing it to facilitate the purchase.
                </p>
                <h3>September 2020</h3>
                <p>Webdesign  | Art Direction</p>
            </div>
        </div>
        <div class="scroll-section secondary" data-scroll-section>
            <div>
                <img alt="page d'accueil de metapoly" :src="image">
            </div>
        </div>
        <div class="scroll-section three" data-scroll-section>
            <div>
                <img alt="metapoly" :src="image2">
                <img class="moving" alt="metapoly" :src="image3">
                <img alt="metapoly" :src="image4">
            </div>
        </div>
        <div class="scroll-section four" data-scroll-section>
            <div>
                <img style="padding-top: 7rem;" alt="metapoly" :src="image5">
            </div>
        </div>
        <div class="scroll-section five" data-scroll-section>
            <div>
                <img style="margin-top: -14rem;" alt="metapoly" :src="image6">
            </div>
        </div>
        <div class="scroll-section six" data-scroll-section>
            <div>
                <img style="padding-top: 9.6rem;" alt="metapoly" :src="image7">
            </div>
        </div>
        <div class="scroll-section seven" data-scroll-section>
            <div>
                <h2>Other project - <span class="transform">Mira</span></h2>
                <router-link class="following" to="/work/mira"><button>View Project</button></router-link>
                <router-link class="following" to="/about"><button class="about">About me</button></router-link>
            </div>
        </div>
    </div>
</template>


<script>
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

import LocomotiveScroll from 'locomotive-scroll';

import image from "@/assets/img/metapoly/Image_1.png"
import image2 from "@/assets/img/metapoly/Image_2.png"
import image3 from "@/assets/img/metapoly/Image_3.png"
import image4 from "@/assets/img/metapoly/Image_4.png"
import image5 from "@/assets/img/metapoly/Image_5.png"
import image6 from "@/assets/img/metapoly/Image_6.png"
import image7 from "@/assets/img/metapoly/Image_7.png"

const initScroll = () => {
    const scroll = new LocomotiveScroll({
        el: document.querySelector('[data-scroll-container]'),
        smooth: true,
        gestureDirection: "both",
        direction: "horizontal",
    });
}

export default {
    name: 'Metapoly',
    data: function () {
        return {
            image: image,
            image2: image2,
            image3: image3,
            image4: image4,
            image5: image5,
            image6: image6,
            image7: image7
        }
    },
    beforeCreate: function() {
        document.body.className = 'metapoly';
    },
    mounted() {
        initScroll();
    },
    updated() {
        initScroll();
    }
}
</script>
<style>
body.metapoly{
    overflow: hidden;
}
body.metapoly .menu-navigation .burger svg > * {
    stroke: #000;
}
</style>
<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';
.scroll-container{
    height: 100vh;
    width: 100%;
    overflow: hidden;
    display: inline-flex;
}
@media screen and(max-width: 1509px){
    #metapoly{
        & .five{
            & img{
                margin-top: -5rem !important;
            }
        }
        & .six{
            min-width: 80% !important;
        }
    }
}
@media screen and(min-width: 1510px){
    #metapoly{
        & .scroll-section{
            background-position-y: bottom !important;
        }
        & .secondary{
            & img{
                width: 1080px !important;
            }
        }
        & .three{
            min-width: 50% !important;
        }
        & .six{
            & img{
                padding-top: 28rem !important;
            }
        }
    }
}
#metapoly{
    & .scroll-section{
        background-image: url("../assets/img/metapoly/parrallax.svg") !important;
        background-repeat: no-repeat;
        background-position-y: bottom;
        background-attachment: fixed;
        box-sizing: content-box;
        height: 100%;
        display: flex;
        align-items: center;
        & img{
            width: 500px;
        }
        h1{
            font-family: 'Oswald', sans-serif !important;
            font-size: 35px;
            font-weight: 200;
            border-bottom: 1px solid black;
            line-height: 2;
        }
        p{
            font-size: 15px;
            font-family: 'Questrial', sans-serif !important;
        }
        h3{
            font-family: 'Oswald', sans-serif !important;
            text-transform: uppercase;
            font-size: 18px;
            font-weight: bold;
        }
    }
    & .start{
        min-width: 30%;
        padding-left: 4rem;
        & > div{
            display: flex;
            flex-direction: column;
            max-width: 386px;
        }
    }
    & .secondary{
        min-width: 70%;
        padding-left: 4rem;
        & > div{
            display: flex;
            & img{
                width: 750px;
                object-fit: contain;
            }
        }
    }
    & .three{
        min-width: 70%;
        & > div{
            display: flex;
        }
        img{
            object-fit: contain;
            height: auto;
            max-width: 318px;
            max-height: 515px;
        }
        img.moving{
            padding-top: 4rem;
        }
    }
    & .four{
        padding-left: 6rem;
        & > div{
            display: flex;
            & img{
                width: 950px;
                object-fit: contain;
            }
        }
    }
    & .five{
        padding-left: 9rem;
        & > div{
            display: flex;
            & img{
                width: 950px;
                object-fit: contain;
            }
        }
    }
    & .six{
        padding-left: 9rem;
        min-width: 65%;
        & > div{
            display: flex;
            & img{
                width: 950px;
                object-fit: contain;
            }
        }
    }
    & .seven{
        min-width: 30%;
        & > div{
            display: flex;
            flex-direction: column;
        }
        & h2{
            font-family: 'Oswald', sans-serif !important;
            font-size: 35px;
            font-weight: 200;
        }
        & span.transform{
            font-weight: 400;
        }
        & .following{
            display: block;
            margin-top: 2rem;
            & :hover{
                background: rgba(209, 209, 209, 0.15);
            }
            & button{
                background-color:#FFFFFF;
                box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
                border: none;
                text-transform: uppercase;
                font-family: 'Oswald', sans-serif !important;
                font-size: 20px;
                font-weight: 400;
                cursor: pointer;
                transition: 0.25s ease;
                width: 257px;
                height: 70px;
            }
            & button.about{
                background-color: #DEDEDE;
                color: #fff;
            }
        }
    }
}
</style>