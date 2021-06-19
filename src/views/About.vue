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
                font-size: 210px;
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
                    padding-top: 5px;
                    margin-top: 0;
                    font-size: 18px;
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
                font-family: 'Oswald', sans-serif !important;
                & .voyages{
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
                        }
                        & img{
                            width: 100%;
                            object-fit: contain;
                            height: 505px;
                            max-width: 533px;
                            max-height: 725px;
                        }
                    }
                }
                & .skill{
                    min-width: 270px;
                    & .info{
                        margin: 3rem 0;
                    }
                    & .titre{
                        font-size: 35px;
                        margin: 0;
                        margin-bottom: 1rem;
                        text-transform: uppercase;
                    }
                    & .direction, .creation{
                        & li{
                            margin: 0;
                            margin-bottom: .5rem;
                            font-size: 18px;
                        }
                    }
                    & .languages{
                        & li{
                            margin: 0;
                        }
                        & span{
                            font-size: 18px;
                            padding-bottom: .5rem;
                            display: block;
                        }
                    }
                    & ul, li{
                        font-size: 18px;
                        list-style: none;
                        text-decoration-style: none;
                        text-decoration: none;
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
            font-family: 'Oswald', sans-serif !important;
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
                    font-size: 35px;
                }
                & .bar{
                    position: relative;
                    cursor: pointer;
                    border-bottom: 1px solid black;
                    & p{
                        width: 100%;
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
                        font-size: 18px;
                    }
                }
                & .date{
                    width: 120px;
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
                        }
                        & .description {
                            font-size: 18px;
                        }
                        & .information{
                            font-size: 18px;
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
                            font-weight: bold;
                            cursor: pointer;
                            transition: 0.25s ease;
                        }
                    }
                }
            }
        }
        
    }
    & .header{
        max-width: calc(100% - 112px);
        width: 100%;
        margin: 0 auto;
        margin-top: 5rem;
        & .container{
            display: block;
            max-width: 1140px;
            margin: 0 auto;
            & h1{
                font-size: 210px;
                text-align: center;
                margin: 0;
            }
            & .resume{
                text-align: center;
                margin: 0 auto;
                font-size: 18px;
                width: 370px;
            }
        }
    }
}

$breakpoint-laptop: 1605px;
$breakpoint-macbook: 1445px;
$breakpoint-ipadpro: 1055px;
$breakpoint-tablet: 768px;
@media screen and(min-width: $breakpoint-laptop){
    & .voyages{
       & .swiper-container, .swiper-wrapper{
            max-width: 533px !important;
        }
        & .swiper-slide{
            & img{
                margin-left: 4rem;
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

export default {
    name: 'About',
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
                        title: "Direction artistic",
                        date: "2021",
                        active: false,
                        information: `
                        2nd year at the Thrive agency now made up of 20 people. With 
                        the evolution of the start-up, I then took on the position of 
                        artistic director, which involves the management of a team of 5 
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
                    lien: "https://projimmoconseil.fr"
                },
                }, 
                {
                projet: {
                    title: "Baco Music",
                    description: "WEB SITES",
                    information: "Label de musique",
                    lien: "https://bacomusic.fr"
                    },
                },
                {
                projet: {
                    title: "TOUCH SENSITY",
                    description: "WEB SITES",
                    information: "Label de musique",
                    lien: "https://touchsensity.com"
                    },
                },
                {
                projet: {
                    title: "MIRA",
                    description: "E-SHOP",
                    information: "Bratisserie artisanale",
                    lien: "https://brasseriemira.fr"
                    },
                },
                {
                projet: {
                    title: "NOS IMPRUDENCES",
                    description: "E-SHOP",
                    information: "Brasserie artisanale",
                    lien: "https://nosimprudences.fr"
                    },
                },
                {
                projet: {
                    title: "ROSE CULOTTE",
                    description: "WEB SITES",
                    information: "Sneakers",
                    lien: "roseculotte.fr"
                    },
                },
                {
                projet: {
                    title: "GINKGO",
                    description: "WEB SITES",
                    information: "Sneakers",
                    lien: "https://ginkgotshirts.com"
                },
                }
            ]
        }
    }
}
</script>
