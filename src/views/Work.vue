<template>
    <div>
        <div class="content-wrap">
            <kinesis-container class="content content--layout">
                <kinesis-element :strength="20" axis="x" class="content__img"><img alt="metapoly" :src="image_one"/></kinesis-element>
                <kinesis-element :strength="50" class="content__title"><h2>METAPOLY</h2></kinesis-element>
                <kinesis-element :strength="10" class="content__author"><p>E-shop</p></kinesis-element>
                <kinesis-element :strength="10" class="content__desc"><p>Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values.</p></kinesis-element>
                <kinesis-element :strength="10" axis="x" class="content__link"><a href="#"><button>Discover</button></a></kinesis-element>
            </kinesis-container>
        </div>
        <div class="content-wrap">
            <kinesis-container class="content content--layout">
                <kinesis-element :strength="20" axis="x" class="content__img"><img alt="metapoly" :src="image_two"/></kinesis-element>
                <kinesis-element :strength="50" class="content__title"><h2>PROJIMMO</h2></kinesis-element>
                <kinesis-element :strength="10" class="content__author"><p>Web site & illustrations</p></kinesis-element>
                <kinesis-element :strength="10" class="content__desc"><p>Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values.</p></kinesis-element>
                <kinesis-element :strength="10" axis="x" class="content__link"><a href="#"><button>Discover</button></a></kinesis-element>
            </kinesis-container>
        </div>
        <div class="content-wrap">
            <kinesis-container class="content content--layout">
                <kinesis-element :strength="20" axis="x" class="content__img"><img alt="metapoly" :src="image_three"/></kinesis-element>
                <kinesis-element :strength="50" class="content__title"><h2>Karma coffee</h2></kinesis-element>
                <kinesis-element :strength="10" class="content__author"><p>Branding & print design</p></kinesis-element>
                <kinesis-element :strength="10" class="content__desc"><p>Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values.</p></kinesis-element>
                <kinesis-element :strength="10" axis="x" class="content__link"><a href="#"><button>Discover</button></a></kinesis-element>
            </kinesis-container>
        </div>
        <div class="content-wrap">
            <kinesis-container class="content content--layout">
                <kinesis-element :strength="20" axis="x" class="content__img"><img alt="metapoly" :src="image_four"/></kinesis-element>
                <kinesis-element :strength="50" class="content__title title_doort"><h2>Doort</h2></kinesis-element>
                <kinesis-element :strength="10" class="content__author"><p>360° project</p></kinesis-element>
                <kinesis-element :strength="10" class="content__desc"><p>Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values.</p></kinesis-element>
                <kinesis-element :strength="10" axis="x" class="content__link"><a href="#"><button>Discover</button></a></kinesis-element>
            </kinesis-container>
        </div>
        <div class="content-wrap">
            <kinesis-container class="content content--layout">
                <kinesis-element :strength="20" axis="x" class="content__img"><img alt="metapoly" :src="image_five"/></kinesis-element>
                <kinesis-element :strength="50" class="content__title"><h2>Brasserie mira</h2></kinesis-element>
                <kinesis-element :strength="10" class="content__author"><p>E-shop & illustrations</p></kinesis-element>
                <kinesis-element :strength="10" class="content__desc"><p>Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values.</p></kinesis-element>
                <kinesis-element :strength="10" axis="x" class="content__link"><a href="#"><button>Discover</button></a></kinesis-element>
            </kinesis-container>
        </div>
        <div class="content-wrap">
            <kinesis-container class="content content--layout">
                <kinesis-element :strength="20" axis="x" class="content__img"><img alt="metapoly" :src="image_six"/></kinesis-element>
                <kinesis-element :strength="50" class="content__title title_camus"><h2>CAMUS</h2></kinesis-element>
                <kinesis-element :strength="10" class="content__author"><p>Branding & print design</p></kinesis-element>
                <kinesis-element :strength="10" class="content__desc"><p>Shirley and Louise are two young women who are launching their designer furniture sales project based on ecological values.</p></kinesis-element>
                <kinesis-element :strength="10" axis="x" class="content__link"><a href="#"><button>Discover</button></a></kinesis-element>
            </kinesis-container>
        </div>
    </div>
</template>

<script>
import image_one from "@/assets/img/projets/Metapoly.png"
import image_two from "@/assets/img/work/work-projimmo.jpg"
import image_three from "@/assets/img/work/work-cafe.jpg"
import image_four from "@/assets/img/projets/Doort.png"
import image_five from "@/assets/img/projets/Mira.png"
import image_six from "@/assets/img/projets/Camus.png"

export default {
    name: 'Work',
    beforeCreate: function() {
        document.body.className = 'work';
    },
    data: function () {
        return {
            image_one: image_one,
            image_two: image_two,
            image_three: image_three,
            image_four: image_four,
            image_five: image_five,
            image_six: image_six
        }
    }
};
</script>

<style>
body.work{
    background-color: #EBEBFF;
}
body.work i.burger svg > * {
    stroke: #000;
}
</style>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';
.content{
    position: relative;
    display: grid;
}
.content-wrap{
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    min-height: 600px;
    pointer-events: none;
 }
.content--layout {
    pointer-events: auto;
    justify-content: center;
    align-content: center;
    grid-template-columns: 242px 242px 242px;
    grid-template-rows: 242px 121px 121px;
    grid-template-areas: "... title title title"
    "author ... desc desc"
    "author ... link link";
}
.content__img{
    height: 484px;
    width: 484px;
    grid-column: 1 / 3;
    grid-row: 1 / 3;
    z-index: 10;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    background-color:transparent;
    & img{
        display: block;
        height: 100%;
        width: 100%;
        object-fit: contain;
    }
}
.content__title {
    grid-area: title;
    line-height: 160px;
    margin: 0;
    z-index: 10;
    cursor: default;
    & h2{
        margin: 0;
        padding-top: 3rem;
        padding-left: 7rem;
        text-transform: uppercase;
        font-size: 150pt;
        font-family: 'AméliaDisplay', sans-serif;
        position: absolute;
        white-space: pre;
    }
}
.content__author {
    grid-area: author;
    margin: 0;
    -webkit-writing-mode: vertical-lr;
    writing-mode: vertical-lr;
    text-align: left;
    z-index: 10;
    cursor: default;
    margin-left: -3rem;
    & p{
        transform: rotate(180deg);
        font-family: 'Oswald', sans-serif !important;
        font-size: 30px;
        font-weight: 200;
        text-transform: uppercase;
        white-space: pre;
        margin: 0;
    }
}
.content__desc {
    grid-area: desc;
    margin: 0;
    z-index: 10;
    padding: 0 1em;
    margin-bottom: -3rem;
    align-self: end;
    cursor: default;
    & p{
        max-width: 297px;
        font-family: 'Questrial', sans-serif !important;
        font-size: 15px;
        font-weight: 400;
        line-height: 1.2;
    }
}
.content__link {
    pointer-events: auto;
    grid-area: link;
    align-self: end;
    justify-self: start;
    z-index: 10;
    padding: 0 1em 0.15em;
    & button{
        background-color:#FFFFFF;
        box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
        border: none;
        text-transform: uppercase;
        font-family: 'Oswald', sans-serif !important;
        font-size: 30px;
        font-weight: 400;
        cursor: pointer;
        transition: 0.25s ease;
        width: 217px;
        height: 70px;
        color: #000;
        text-decoration: none;
        &:hover{
            background-color: $mauve;
        }
    }
}
.title_camus, .title_doort{
    & h2{
        padding-left: 10rem;
    }
}
</style>