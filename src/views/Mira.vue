<template>
    <div id="mira" class="scroll-container" data-scroll-container>
        <div class="scroll-section start" data-scroll-section>
            <div>
                <h1>E-shop - mira</h1>
                <p>
                    After creating an e-commerce like their showcase site, I created for Mira, a subscription page highlighting the mystery and exclusivity of this offer. The main idea was to highlight their flagship asset : spring water. </p><p>
I am currently working on a redesign of e-commerce on a white background, which I can’t wait to present. The Mira universe is turned towards originality. Highlighting containers worked by artists, it wants to be a « cabinet of curiosity ». </p><p>
Based on a dark background I had, during this redesign, to rework a specific web charter preserving the spirit while focusing on the UX of a classic e-shop..
                </p>
                <h3>January 2020</h3>
                <p>Webdesign  | Art Direction | Illustrations</p>
            </div>
        </div>
        <div class="scroll-section secondary" data-scroll-section>
            <div>
                <img alt="page d'accueil de mira" :src="image">
            </div>
        </div>
        <div class="scroll-section three" data-scroll-section>
            <div>
                <img class="image_2" alt="mira" :src="image2">
                <img class="image_3" alt="mira" :src="image3">
                <img class="image_4" alt="mira" :src="image4">
                <img class="image_5" alt="mira" :src="image5">
            </div>
        </div>
        <div class="scroll-section four" data-scroll-section>
            <div>
                <img class="image_6" alt="mira" :src="image6">
                <img class="image_7" alt="mira" :src="image7">
            </div>
        </div>
        <div class="scroll-section five" data-scroll-section>
            <div>
                <h2>Other project - <span class="transform">Metapoly</span></h2>
                <router-link class="following" to="/work/metapoly"><button>View Project</button></router-link>
                <router-link class="following" to="/about"><button class="about">About me</button></router-link>
            </div>
        </div>
    </div>
</template>


<script>
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

import LocomotiveScroll from 'locomotive-scroll';

import image from "@/assets/img/mira/Image_1.png"
import image2 from "@/assets/img/mira/Image_2.png"
import image3 from "@/assets/img/mira/Image_3.png"
import image4 from "@/assets/img/mira/Image_4.png"
import image5 from "@/assets/img/mira/Image_5.png"
import image6 from "@/assets/img/mira/Image_6.png"
import image7 from "@/assets/img/mira/Image_7.png"

const initScroll = () => {
    const scroll = new LocomotiveScroll({
        el: document.querySelector('[data-scroll-container]'),
        smooth: true,
        gestureDirection: "both",
        direction: "horizontal",
    });
}

export default {
    name: 'mira',
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
        document.body.className = 'mira';
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
body.mira{
    overflow: hidden;
}
body.mira .menu-navigation .burger svg > * {
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
    #mira{
        & .three{
            min-width: auto !important;
        }
        & .four{
            padding-left: 5rem !important;
            min-width: 60% !important;
            & img.image_7{
                padding-top: 4rem !important;
                object-fit: cover !important;
            }
        }
    }
}
@media screen and(min-width: 1510px){
    #mira{
        & .scroll-section{
            background-position-y: bottom !important;
        }
        & .secondary{
            & img{
                width: 1080px !important;
            }
        }
        & .three{
            //min-width: 50% !important;
        }
        & .six{
            & img{
                //padding-top: 28rem !important;
            }
        }
    }
}
#mira{
    & .scroll-section{
        background-image: url("../assets/img/mira/parrallax.svg") !important;
        background-repeat: no-repeat;
        background-position-y: bottom;
        background-attachment: fixed;
        box-sizing: content-box;
        height: 100%;
        display: flex;
        align-items: center;
        margin-right: -1px;
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
            font-weight: 400;
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
        min-width: 90%;
        & > div{
            display: flex;
        }
        img{
            object-fit: contain;
            height: auto;
        }
        img.image_2{
            max-width: 456px;
            max-height: 264px;
        }
        img.image_3{
            padding-top: 7rem;
            max-width: 456px;
            max-height: 329px;
        }
        img.image_4{
            padding-top: -2rem;
            max-width: 456px;
            max-height: 225px;
        }
        img.image_5{
            padding-top: 18rem;
            margin-left: -14rem;
            max-width: 456px;
            max-height: 225px;
        }
    }
    & .four{
        padding-left: 0rem;
        min-width: 50%;
        & > div{
            display: flex;
            & img.image_6{
                width: 399px;
                max-height: 658px;
                object-fit: contain;
            }
            & img.image_7{
                padding-top: 2rem;
                margin-left: 3rem;
                width: 170px;
                max-height: 328px;
                object-fit: contain;
            }
        }
    }
    & .five{
        min-width: 50%;
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