<template>
    <div id="about">
        <img class="wave" :src="image"/>
        <div class="header">
            <div class="container">
                <!-- Image -->
                <h1>DAGs !</h1>
                <p class="resume">
                    {{ presentation }}
                </p>
            </div>
        </div>
        <div class="container">
            <section class="row about-me">
                <h2>About me</h2>
                <div class="containt">
                    <p>
                        Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
                    </p>
                    <p>
                        Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
                    </p>
                    <p>
                        Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
                    </p>
                </div>
            </section>
            <section class="row references">
                <h2>References</h2>
                <div class="containt projets">
                    <li class="card" v-for="item in experiences" :key="item.projets">
                        <div class="info">
                            <p class="titre">{{ item.projet.title }}</p>
                            <p class="description">{{ item.projet.description }}</p>
                            <p class="information">{{ item.projet.information }}</p>
                        </div>
                        <div class="website">
                            <a :href="`${item.projet.lien}`"><button>Website</button></a>
                        </div>
                    </li>
                </div>
            </section>
            <section class="row skills">
                <h2>Skills</h2>
                <div class="containt">
                    
                </div>
            </section>
            <section class="row experiences">
                <h2>Experiences</h2>
                <div class="containt">
                    
                </div>
            </section>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';
#about{
    position: relative;
    & .wave{
        position: absolute;
        left: -3rem;
        top: 20rem;
        z-index: -1;
    }
    & .container{
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
            & .containt{
                & p{
                    margin-top: 0;
                    font-size: 18px;
                }
            }
        }
        & .references{
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
        margin-top: 300px;
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
</style>

<script>
import image from "@/assets/img/about-wave.svg"

export default {
    data: function () {
        return {
            image: image,
            presentation: "I am Jeanne, graphic designer, illustrator and web designer in the direction of Amsterdam. This job for me is to help brands make a difference, my goal is your smile.",
            experiences: [
                {
                projet: {
                    title: "Projimmo",
                    description: "WEB SITE  ILLUSTRATIONS  ANIMATIONS",
                    information: "Groupe immobilier",
                    lien: "test"
                },
                }, 
                {
                projet: {
                    title: "Baco Music",
                    description: "WEB SITES",
                    information: "Label de musique",
                    lien: ""
                    },
                },
                {
                projet: {
                    title: "TOUCH SENSITY",
                    description: "WEB SITES",
                    information: "Label de musique",
                    lien: ""
                    },
                },
                {
                projet: {
                    title: "MIRA",
                    description: "E-SHOP",
                    information: "Bratisserie artisanale",
                    lien: ""
                    },
                },
                {
                projet: {
                    title: "NOS IMPRUDENCES",
                    description: "E-SHOP",
                    information: "Brasserie artisanale",
                    lien: ""
                    },
                },
                {
                projet: {
                    title: "PERAMOR",
                    description: "IDENTITY",
                    information: "Sneakers",
                    lien: ""
                    },
                },
                {
                projet: {
                    title: "ROSE CULOTTE",
                    description: "WEB SITES",
                    information: "Sneakers",
                    lien: ""
                    },
                },
                {
                projet: {
                    title: "GINKGO",
                    description: "WEB SITES",
                    information: "Sneakers",
                    lien: ""
                },
                }
            ]
        }
    }
}
</script>