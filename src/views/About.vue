<template>
    <div id="about">
        <img class="wave" :src="image"/>
        <div class="header">
            <div class="container">
                <img alt="autoportrait Jeanne" class="autoportrait" :src="image_jane"/>
                <h1>DAG !</h1>
                <p class="resume">
                    {{ presentation }}
                </p>
            </div>
        </div>
        <div class="container">
            <section class="row about-me">
                <h2 style>About me</h2>
                <div class="containt">
                    <p>
                       Passionate about design, I have made it my career goal since the beginning of my studies. I am a graphic designer and web designer soon to settle in Amsterdam. After almost 2 years of experience in a communication agency specializing in digital, I fly to the Netherlands to immerse myself in an important graphic culture. I was able to work as an artistic director and graphic designer for regional and national clients, in print and digital. Today, I want to develop my activity for several reasons that I could sum up in 3 points: communication, teamwork and dynamism.
                    </p>
                    <p>
                        This book is meant to reflect my inspirations, my experience and my ideas. It brings together a selection of my most recent projects. If you find my profile interesting, I will be happy to meet you and explain my motivations to join your team.
                    </p>
                </div>
            </section>
            <!-- MACHINE A LAVER -->
            <section class="row skills">
                <h2>Skills</h2>
                <div class="containt">
                    <div class="skill">
                        <div class="info-first">
                            <p class="titre">Artistic direction</p>
                            <ul class="direction">
                                <li>Positioning, brand promotion</li>
                                <li>Creative campaign concept</li>
                                <li>Social media editorial strategy</li>
                                <li>Graphic charter, brand DNA</li>
                                <li>Needs analysis, diagnosis</li>
                                <li>Team management, project planning</li>
                            </ul>
                        </div>
                        <div class="info">
                            <p class="titre">design creation</p>
                            <ul class="creation">
                                <li>Branding identity, logotype</li>
                                <li>UX/UI design</li>
                                <li>Multi media design print</li>
                                <li>Illustration, graphic design</li>
                                <li>Photography & video editing</li>
                                <li>Design set, scenographic styling</li>
                            </ul>
                        </div>
                        <div class="info">
                            <p class="titre">LANGUAGES</p>
                            <ul class="languages">
                                <li>FRENCH</li>
                                <span>Native language</span>
                                <li>ENGLISH</li>
                                <span>Elementary A2</span>
                                <li>SPANISH</li>
                                <span>Intermediate B1</span>
                                <li>DUTCH</li>
                                <span>Notions A1</span>
                            </ul>
                        </div>
                    </div>
                    <div class="voyages">
                        <div class="swiper-container" id="swiper-voyage">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide">
                                    <img alt="photographie" class="photo-voyage" :src="image_one"/>
                                    <span>Cadiz, Spain</span>
                                </div>
                                <div class="swiper-slide">
                                    <img alt="photographie" class="photo-voyage" :src="image_two"/>
                                    <span>Randa, Switzerland</span>
                                </div>
                                <div class="swiper-slide">
                                    <img alt="photographie" class="photo-voyage" :src="image_three"/>
                                    <span>Porto, Portugal</span>
                                </div>
                                <div class="swiper-slide">
                                    <img alt="photographie" class="photo-voyage" :src="image_four"/>
                                    <span>Roma, Italy</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            <section class="row experiences">
                <h2>Experiences</h2>
                <div class="containt contenu">
                    <li :class="[`index--${index}`]" class="card" v-for="(item, index) in experiences" :key="index.contenu">
                        <div class="info">
                            <span class="title date">{{ item.contenu.date }}</span>
                            <div style="width: 500px;">
                                <div v-on:click="item.contenu.active = !item.contenu.active" class="bar">
                                    <p class="title">{{ item.contenu.title }}</p>
                                    <svg v-show="!item.contenu.active" class="circle-icon" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 21 21">
                                        <g id="Groupe_185" data-name="Groupe 185" transform="translate(-1596 -3362)">
                                            <g id="Ellipse_7" data-name="Ellipse 7" transform="translate(1596 3362)" fill="#fff" stroke="#000" stroke-linecap="round" stroke-width="1">
                                            <circle cx="10.5" cy="10.5" r="10.5" stroke="none"/>
                                            <circle cx="10.5" cy="10.5" r="10" fill="none"/>
                                            </g>
                                            <path id="Tracé_212" data-name="Tracé 212" d="M0,0H8.658" transform="translate(1602.171 3372.5)" fill="none" stroke="#000" stroke-linecap="round" stroke-width="1"/>
                                            <path id="Tracé_213" data-name="Tracé 213" d="M0,0H8.658" transform="translate(1606.5 3368.171) rotate(90)" fill="none" stroke="#000" stroke-linecap="round" stroke-width="1"/>
                                        </g>
                                    </svg>
                                    <svg v-show="item.contenu.active" class="circle-icon" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 21 21">
                                        <g id="Groupe_184" data-name="Groupe 184" transform="translate(-1596 -3362)">
                                            <g id="Ellipse_7" data-name="Ellipse 7" transform="translate(1596 3362)" fill="#fff" stroke="#000" stroke-linecap="round" stroke-width="1">
                                            <circle cx="10.5" cy="10.5" r="10.5" stroke="none"/>
                                            <circle cx="10.5" cy="10.5" r="10" fill="none"/>
                                            </g>
                                            <line id="Ligne_21" data-name="Ligne 21" x2="8.658" transform="translate(1602.171 3372.5)" fill="none" stroke="#000" stroke-linecap="round" stroke-width="1"/>
                                        </g>
                                    </svg>
                                </div>
                                <div v-show="item.contenu.active" class="information">
                                    <p>{{ item.contenu.information }}</p>
                                </div>
                            </div>
                        </div>
                    </li>
                </div>
            </section>
            <section class="row references">
                <h2>References</h2>
                <div class="containt">
                    <li class="card" v-for="(item, index) in references" :key="index.projets">
                        <div class="info">
                            <p class="titre">{{ item.projet.title }}</p>
                            <p class="description">{{ item.projet.description }}</p>
                            <p class="information">{{ item.projet.information }}</p>
                        </div>
                        <div class="website">
                            <a target="_blank" :href="`${item.projet.lien}`"><button>Website</button></a>
                        </div>
                    </li>
                </div>
            </section>
        </div>
        <div class="me-contacter">
            <Contacts/>
        </div>
        <div class="page-footer">
            <span>© Jeanne Chevallier 2021</span>
            <div>
                <a target="_blank" href="https://www.linkedin.com/in/jeanne-chevallier-106969133/">
                    <svg xmlns="http://www.w3.org/2000/svg" width="35.744" height="31.626" viewBox="0 0 35.744 31.626">
                        <g id="Groupe_207" data-name="Groupe 207" transform="translate(0 -2.06)">
                            <path id="Tracé_214" data-name="Tracé 214" d="M.589-3.352H8V17.775H.589ZM4.3-13.851a4.073,4.073,0,0,1,4.292,3.806A4.075,4.075,0,0,1,4.3-6.234,4.077,4.077,0,0,1,0-10.045a4.075,4.075,0,0,1,4.3-3.806" transform="translate(0 15.911)"/>
                            <g id="Groupe_198" data-name="Groupe 198" transform="translate(12.652 12.036)">
                            <path id="Tracé_215" data-name="Tracé 215" d="M0,.308H7.1V3.2h.1c.99-1.661,3.4-3.412,7.011-3.412,7.5,0,8.879,4.373,8.879,10.061V21.435h-7.4V11.162c0-2.451-.056-5.6-3.85-5.6C7.989,5.561,7.4,8.229,7.4,10.984v10.45H0Z" transform="translate(0 0.215)"/>
                            </g>
                        </g>
                    </svg>
                </a>
                <a target="_blank" href="http://instagram.com/lajanecy/">
                    <svg xmlns="http://www.w3.org/2000/svg" width="35.745" height="35.745" viewBox="0 0 35.745 35.745">
                        <g id="Groupe_208" data-name="Groupe 208" transform="translate(-59.628 0)">
                            <g id="Groupe_202" data-name="Groupe 202" transform="translate(84.868 6.383)">
                            <path id="Tracé_220" data-name="Tracé 220" d="M1.234,0a2.1,2.1,0,1,0,2.1,2.1A2.1,2.1,0,0,0,1.234,0" transform="translate(0.862)"/>
                            </g>
                            <g id="Groupe_203" data-name="Groupe 203" transform="translate(68.845 9.07)">
                            <path id="Tracé_221" data-name="Tracé 221" d="M5.184,0a8.8,8.8,0,1,0,8.8,8.8A8.814,8.814,0,0,0,5.184,0m0,14.441A5.639,5.639,0,1,1,10.821,8.8a5.645,5.645,0,0,1-5.637,5.637" transform="translate(3.62)"/>
                            </g>
                            <path id="Tracé_222" data-name="Tracé 222" d="M14.725,21.047H.454A10.749,10.749,0,0,1-10.283,10.31V-3.961A10.751,10.751,0,0,1,.454-14.7H14.725A10.751,10.751,0,0,1,25.462-3.961V10.31A10.749,10.749,0,0,1,14.725,21.047M.454-11.335A7.382,7.382,0,0,0-6.92-3.961V10.31A7.382,7.382,0,0,0,.454,17.684H14.725A7.382,7.382,0,0,0,22.1,10.31V-3.961a7.382,7.382,0,0,0-7.374-7.374Z" transform="translate(69.911 14.698)"/>
                        </g>
                    </svg>
                </a>
                <a target="_blank" href="https://www.behance.net/jeannecheve337">
                    <svg xmlns="http://www.w3.org/2000/svg" width="44.472" height="27.788" viewBox="0 0 44.472 27.788">
                        <g id="Groupe_210" data-name="Groupe 210" transform="translate(-119.257 9.709)">
                            <g id="Groupe_208" data-name="Groupe 208" transform="translate(0 -14.698)">
                            <g id="Groupe_209" data-name="Groupe 209">
                                <g id="Groupe_199" data-name="Groupe 199" transform="translate(119.257 4.989)">
                                <path id="Tracé_216" data-name="Tracé 216" d="M13.183,12.145a6.314,6.314,0,0,1-2.641,5.324,9.079,9.079,0,0,1-2.858,1.369,12.388,12.388,0,0,1-3.463.469H-9.206V-8.481H5.668a5.493,5.493,0,0,1,2.622.625,6.535,6.535,0,0,1,2,1.625A7.45,7.45,0,0,1,11.558-3.96a7.653,7.653,0,0,1,.45,2.563,7.562,7.562,0,0,1-1.017,3.816A6.2,6.2,0,0,1,8.017,5.06a7.147,7.147,0,0,1,3.777,2.524,7.31,7.31,0,0,1,1.389,4.56M-3.8-3.863V3.144H3.4A3.2,3.2,0,0,0,5.726,2.2,3.444,3.444,0,0,0,6.685-.38,3.565,3.565,0,0,0,5.8-2.924a2.861,2.861,0,0,0-2.172-.939ZM7.743,11.126A4.062,4.062,0,0,0,7.487,9.7,3.967,3.967,0,0,0,6.8,8.5a3.228,3.228,0,0,0-1.019-.8A2.861,2.861,0,0,0,4.493,7.41H-3.8v7.318H4.221a3.486,3.486,0,0,0,1.389-.275,3.336,3.336,0,0,0,1.116-.761,3.735,3.735,0,0,0,1.017-2.566" transform="translate(9.206 8.481)"/>
                                </g>
                                <g id="Groupe_200" data-name="Groupe 200" transform="translate(142.878 12.186)">
                                <path id="Tracé_217" data-name="Tracé 217" d="M6.163,12.125a11.059,11.059,0,0,1-4.324-.815,9.751,9.751,0,0,1-5.4-5.479A10.512,10.512,0,0,1-4.3,1.922a11.048,11.048,0,0,1,.722-4,9.722,9.722,0,0,1,5.4-5.555A11.023,11.023,0,0,1,6.2-8.467a10.757,10.757,0,0,1,4.341.834c4.2,1.829,6.175,5.9,5.992,10.314a3.777,3.777,0,0,1-.095.759H1.083a5.876,5.876,0,0,0,.569,2.087A5.111,5.111,0,0,0,4.458,8.068a5.375,5.375,0,0,0,1.895.34,5.846,5.846,0,0,0,2.862-.739,3.917,3.917,0,0,0,1.841-1.953L15.417,6.93a8.858,8.858,0,0,1-3.509,3.736,10.872,10.872,0,0,1-5.744,1.459M11.322.142A5.283,5.283,0,0,0,9.673-3.443,5.05,5.05,0,0,0,6.127-4.79a5.1,5.1,0,0,0-1.916.36A5,5,0,0,0,2.637-3.423,5.179,5.179,0,0,0,1.518-1.869,5.463,5.463,0,0,0,1.005.14H11.322Z" transform="translate(4.304 8.467)"/>
                                </g>
                            </g>
                            </g>
                            <path id="Tracé_219" data-name="Tracé 219" d="M60.3-12.1H73.6v3.3H60.3Z" transform="translate(86.354 3.715)"/>
                        </g>
                    </svg>
                </a>
            </div>
        </div>
    </div>
</template>

<style>
    body.about .menu-navigation .burger svg > * {
        stroke: #000;
    }
</style>
<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';
#about{
    position: relative;
    overflow-y: hidden;
    & .wave{
        position: absolute;
        left: -3rem;
        top: 40rem;
        z-index: -1;
    }
    & .container{
        & img.autoportrait{
            max-width: 905px;
            height: 100%;
            object-fit: contain;
            width: 100%;
            margin: 0 auto;
            display: block;
            margin-bottom: 5rem;
        }
        & section.row{
            margin: 300px auto;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: flex-start;
            column-gap: 50px;
            & h2{
                margin: 0;
                flex: 1;
                font-family: "AméliaDisplay";
                font-size: 150px;
                letter-spacing: -5px;
                text-transform: uppercase;
                text-align: right;
            }
            & .containt{
                flex: 1;
                margin-right: 70px;
            }
        }
        & .about-me{
            & h2{
                line-height: 1;
            }
            & .containt{
                & p{
                    font-family: 'Questrial', sans-serif !important;
                    padding-top: 5px;
                    margin-top: 0;
                    font-size: 16px;
                    max-width: 58%;
                }
            }
        }
        & section.skills{
            & h2{
                line-height: 1;
            }
            & .containt{
                overflow: hidden;
                display: flex;
                flex-direction: row;
                .voyages{
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    & .swiper-container, .swiper-wrapper{
                        max-width: 390px;
                    }
                    & .swiper-slide{
                        display: flex;
                        flex-direction: column;
                        justify-content: flex-end;
                        max-width: 100%;
                        & span{
                            display: block;
                            margin-right: 0;
                            margin-left: auto;
                            width: auto;
                            font-family: 'Oswald', sans-serif !important;
                        }
                        & img{
                            width: 100%;
                            object-fit: contain;
                            height: 505px;
                            max-width: 533px;
                            max-height: 725px;
                            object-position: right;
                        }
                    }
                }
                & .skill{
                    min-width: 270px;
                    & .info{
                        margin: 3rem 0;
                    }
                    & .titre{
                        font-size: 26px;
                        font-family: 'Oswald', sans-serif !important;
                        margin: 0;
                        margin-bottom: 1rem;
                        text-transform: uppercase;
                    }
                    & .direction, .creation{
                        & li{
                            margin: 0;
                            margin-bottom: .5rem;
                            font-size: 15px;
                            font-family: 'Questrial', sans-serif !important;
                        }
                    }
                    & .languages{
                        & li{
                            margin: 0;
                            font-family: 'Questrial', sans-serif !important;
                        }
                        & span{
                            font-size: 15px;
                            padding-bottom: .5rem;
                            display: block;
                        }
                    }
                    & ul, li{
                        font-size: 15px;
                        list-style: none;
                        text-decoration-style: none;
                        text-decoration: none;
                        font-family: 'Questrial', sans-serif !important;
                    }
                    & ul{
                        margin: 0;
                        padding: 0;
                    }
                }
            }
        }
        & section.experiences{
            margin-top: 400px;
            & h2{
                line-height: 1;
            }
            & .containt{
                & li{
                    list-style: none;
                    text-decoration-style: none;
                    text-decoration: none;
                }
                & .card{
                    margin-bottom: 2rem;
                }
                & .title{
                    font-size: 26px;
                }
                & .bar{
                    position: relative;
                    cursor: pointer;
                    border-bottom: 1px solid black;
                    & p{
                        width: 100%;
                        font-family: 'Oswald', sans-serif !important;
                        margin: 0;
                        text-transform: uppercase;
                    }
                    & .circle-icon{
                        position: absolute;
                        right: 0;
                        bottom: .5rem;
                    }
                }
                & .information{
                    & p{
                        font-size: 16px;
                        font-family: 'Questrial', sans-serif !important;
                    }
                }
                & .date{
                    width: 120px;
                    font-family: 'Oswald', sans-serif !important;
                }
                & .info{
                    display: flex;
                    flex-direction: row;
                    align-items: baseline;
                }
            }
        }
        & section.references{
            margin-top: 500px;
            margin-bottom: 1rem;
            & .containt{
                & li{
                    list-style: none;
                    text-decoration-style: none;
                    text-decoration: none;
                }
                & .card{
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    width: 450px;
                    align-items: center;
                    margin-bottom: 5rem;
                    & .info{
                        display: inline;
                        & p{
                            margin: 0;
                        }
                        & .titre{
                            font-size: 35px;
                            text-transform: uppercase;
                            font-family: 'Oswald', sans-serif !important;
                        }
                        & .description {
                            font-size: 16px;
                            font-family: 'Questrial', sans-serif !important;
                        }
                        & .information{
                            font-size: 16px;
                            font-family: 'Questrial', sans-serif !important;
                        }
                    }
                    & .website{
                        display: block;
                        & a{
                            & :hover{
                                background: $mauve;
                            }
                        }
                        & button{
                            box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
                            background: none;
                            border: none;
                            padding: 1rem;
                            text-transform: uppercase;
                            font-family: 'Oswald', sans-serif !important;
                            font-size: 30px;
                            font-weight: 400;
                            cursor: pointer;
                            transition: 0.25s ease;
                        }
                    }
                }
            }
        }
        
    }
    & .me-contacter{
        height: 800px;
    }
    & .page-footer{
        max-width: calc(100% - 112px);
        width: 100%;
        position: absolute;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin: 0 auto;
        left: 0;
        right: 0;
        bottom: 1px;
        & span{
            font-family: 'Questrial', sans-serif !important;
            font-size: 18px;
        }
        & svg{
            padding-left: 1rem;
        }
    }
    & .header{
        max-width: calc(100% - 112px);
        width: 100%;
        margin: 0 auto;
        margin-top: 11rem;
        & .container{
            display: block;
            max-width: 1140px;
            margin: 0 auto;
            & h1{
                font-size: 150px;
                text-align: center;
                margin: 0;
            }
            & .resume{
                text-align: center;
                margin: 0 auto;
                font-size: 16px;
                width: 370px;
                font-family: 'Questrial', sans-serif !important;
            }
        }
    }
}

$breakpoint-laptop: 1605px;
$breakpoint-macbook: 1445px;
$breakpoint-ipadpro: 1055px;
$breakpoint-tablet: 768px;
@media screen and(min-width: $breakpoint-laptop){
    .voyages{
       & .swiper-container, .swiper-wrapper{
            max-width: 533px !important;
        }
        & .swiper-slide{
            & img{
                margin-left: 3rem;
                margin-bottom: 41px;
                height: 640px !important;
            }
        }
    }
}
@media (min-width: $breakpoint-tablet) and (max-width: $breakpoint-laptop) {
    #about{
        & .container{
            & img.autoportrait{
                width: 50%;
            }
        }
        .about-me {
            & .containt{
                & p{
                    max-width: 74% !important;
                }
            }
        }
    }
}

</style>
<style>
body.about #footer svg{
   display: none;
}
body.about .swiper-button-next{
  background-image: url("../assets/img/arrow-next.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
}
body.about .swiper-button-prev{
  background-image: url("../assets/img/arrow-prev.png") !important;
  background-repeat: no-repeat;
  background-size: contain;
}
body.about .swiper-button-prev::after, .swiper-button-next::after{
  display: none !important;
}
</style>

<script>
import image from "@/assets/img/about-wave.svg"
import image_jane from "@/assets/img/about/Autoportrait_Jeanne.png"

import image_one from "@/assets/img/about/voyage_un.png"
import image_two from "@/assets/img/about/voyage_deux.png"
import image_three from "@/assets/img/about/voyage_trois.png"
import image_four from "@/assets/img/about/voyage_quatre.png"


import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

const initSwiperVoyage = () => {
    // Init Swiper
    let swiper = new Swiper("#swiper-voyage", {
        // Optional parameters
        loop: true,
        slidesPerView: 1,
        effect: "fade",
        fadeEffect: {
          crossFade: true,
        },
        grabCursor: true,
    });
};
import Contacts from '@/components/contact.vue'

export default {
    name: 'About',
    components: {
        Contacts,
    },
    beforeCreate: function() {
        document.body.className = 'about';
    },
    mounted() {
        initSwiperVoyage();
    },
    updated() {
        initSwiperVoyage();
    },
    data: function () {
        return {
            image: image,
            image_jane: image_jane,
            image_one: image_one,
            image_two: image_two,
            image_three: image_three,
            image_four: image_four,
            presentation: "I am Jeanne, graphic designer, illustrator and web designer in the direction of Amsterdam. This job for me is to help brands make a difference, my goal is your smile.",
            experiences: [
                {
                    contenu: {
                        title: "Art Direction",
                        date: "2021",
                        active: false,
                        information: `
                        2nd year at the Thrive agency now made up of 20 people. With 
                        the evolution of the start-up, I then took on the position of 
                        art direction, which involves the management of a team of 5 
                        people. I am in charge of the creation of coherent and relevant 
                        graphic universes but also of the management of the customer 
                        relationship at the level of the pole.
                        `,
                    },
                },
                {
                    contenu: {
                        title: "Webdesigner",
                        date: "2019",
                        active: false,
                        information: `Arrival at the Thrive agency then composed of 7 people during 
                        my work-study training. My missions are the design of web 
                        interfaces, the creation of identity as well as the layout on 
                        printed and digital media`,
                    },
                },
                {
                    contenu: {
                        title: "Art school",
                        date: "2019",
                        active: false,
                        information: `One year of artistic training on graphics, its codes and techniques.`,
                    },
                },
                {
                    contenu: {
                        title: "Cinema operator",
                        date: "2019",
                        active: false,
                        information: `Working in the cinema was a very rich experience, it allowed me 
                        to learn how to manage several tasks without being 
                        overwhelmed. Busy hours are times when you have to stay well 
                        organized, focused and always maintain good communication 
                        with your team and clients
                        `,
                    },
                },
                {
                    contenu: {
                        title: "Design graphic school",
                        date: "2018",
                        active: false,
                        information: `A year of training on creation software, the rules of graphics and 
                        artistic openness. I had the chance to be in a class of 3 people 
                        which allowed me to be truly accompanied to the pixel in my 
                        creations.`,
                    },
                },
                {
                    contenu: {
                        title: "Rental management coordinator",
                        date: "2018",
                        active: false,
                        information: `Rental management is a job that taught me a lot about human 
                        contact. Often pleasant, it also happens to me to manage more 
                        difficult situations where assertiveness was essential.`,
                    },
                },
                {
                    contenu: {
                        title: "Commercial & concept redaction",
                        date: "2017",
                        active: false,
                        information: `During my internship at the Demoiselle radio station, I took on 
                        the role of sales representative. Between negotiation, 
                        prospecting and sales, I was responsible for writing advertising 
                        spots. Radio is not an easy communication tool that it was 
                        particularly interesting to develop during this experience.`,
                    },
                },
                {
                    contenu: {
                        title: "Graphist assistant",
                        date: "2017",
                        active: false,
                        information: `During this first internship in creation, I had to design illustrations, create visual identities as well as participate in the development of packaging in the context of the food and cosmetics sector.`,
                        information: `This experience confirmed my wish for guidance in the creative field of communication. My first career objective was print and more particularly a specialization in packaging, because it is complex and full of constraints but also necessary and functional in addition to its aesthetic need which guides consumers’ choice.`
                    },
                },
                {
                    contenu: {
                        title: "Communications Officer",
                        date: "2016",
                        active: false,
                        information: `During the campaign to launch a new point of sale, I worked on the communication of Pizzeria Giovanni from a strategic and creative point of view.`,
                        information: `In autonomy, this project was surely the most formative of my beginnings. Managing the relations of service providers and ensuring a clean final state of the submitted files requires a rigor that I was given to acquire thanks to the confidence and the patience of the pizzeria Giovanni when I started as a graphic designer. independent.`
                    },
                },
                {
                    contenu: {
                        title: "Sub de pub",
                        date: "2016",
                        active: false,
                        information: `BTS communication, 2 years of training in marketing strategy and advertising analysis. Here I learn how to work on a concept and target an audience so that the communication has a real impact on the consumer`,
                    },
                },
                {
                    contenu: {
                        title: "end of my secondary studies",
                        date: "2016",
                        active: false,
                        information: `First steps in the world of design, I then discovered the 
                        profession of graphic designers and all professions 
                        related to printing
                        `,
                    },
                },
                {
                    contenu: {
                        title: "trainee in printing",
                        date: "2013",
                        active: false,
                        information: `First steps in the world of design, I then discovered the 
                        profession of graphic designers and all professions 
                        related to printing
                        `,
                    },
                },
            ],
            references: [
                {
                projet: {
                    title: "Projimmo",
                    description: "WEB SITE  ILLUSTRATIONS  ANIMATIONS",
                    information: "Groupe immobilier",
                    lien: "https://www.projimmoconseil.fr"
                },
                }, 
                {
                projet: {
                    title: "Baco Music",
                    description: "WEB SITE",
                    information: "Label de musique",
                    lien: "https://bacomusic.fr"
                    },
                },
                {
                projet: {
                    title: "TOUCH SENSITY",
                    description: "WEB SITE",
                    information: "Materials company",
                    lien: "https://touchsensity.com"
                    },
                },
                {
                projet: {
                    title: "MIRA",
                    description: "E-SHOP",
                    information: "Brasserie artisanale",
                    lien: "https://brasseriemira.fr"
                    },
                },
                {
                projet: {
                    title: "NOS IMPRUDENCES",
                    description: "E-SHOP",
                    information: "Online clothing sales",
                    lien: "https://nosimprudences.fr"
                    },
                },
                /*{
                projet: {
                    title: "ROSE CULOTTE",
                    description: "WEB SITE",
                    information: "Music band",
                    lien: "https://roseculotte.fr"
                    },
                },*/
                {
                projet: {
                    title: "GINKGO",
                    description: "WEB SITE",
                    information: "Online clothing sales",
                    lien: "https://ginkgotshirts.com"
                },
                }
            ]
        }
    }
}
</script>
