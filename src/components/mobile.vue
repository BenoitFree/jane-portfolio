<template>
    <div class="jane-is-mobile">
        <img class="profil-insta" alt="Photo de profil de lajanecy" :src="logoinsta">
        <h1 class="title-mobile">Retrouvez-moi sur Instagram</h1>
        <a class="instagram-link" title="Alexo88, Public domain, via Wikimedia Commons" href="https://www.instagram.com/lajanecy/"><img alt="Instagram" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Instagram.svg/512px-Instagram.svg.png"><span>lajanecy</span></a>
    </div>
</template>
<style>
    body{
        margin: 0;
    }
</style>
<style lang="scss" scoped>
    .jane-is-mobile{
        background: #000;
        width: 100%;
        height: 100vh;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        & img.profil-insta{
            height: 200px;
            margin-top: -1rem;
            margin-bottom: 4rem;
        }
        & h1.title-mobile{
            font-size: 48px;
            color: #fff;
            font-family: "AméliaDisplay" !important;
        }
        & a.instagram-link{
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            & img{
                width: 30px;
            } 
            & span{
                padding-left: 1rem;
                font-size: 28px;
                color: #fff;
                font-family: 'Oswald', sans-serif !important;
            }
        }
    }
    
</style>
<script>
import logoinsta from "@/assets/img/jane-logo-insta.jpg";
    export default {
    data: function () {
        return {
        logoinsta: logoinsta,
        }
    }
}
</script>