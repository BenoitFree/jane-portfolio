<template>
<div>
    <div id="nav" class="menu-navigation">
        <router-link to="/">
            <h1 class="logo">
                <svg v-bind:class="{ icon_is_close: isActive }" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="202.312" height="104.576" viewBox="0 0 202.312 104.576">
                    <defs>
                        <clipPath id="clip-path">
                        <path id="Tracé_52" data-name="Tracé 52" d="M0-39.212H202.312V-143.788H0Z" transform="translate(0 143.788)" fill="none"/>
                        </clipPath>
                    </defs>
                    <g id="Groupe_55" data-name="Groupe 55" transform="translate(0 143.788)">
                        <g id="Groupe_54" data-name="Groupe 54" transform="translate(0 -143.788)" clip-path="url(#clip-path)">
                        <g id="Groupe_50" data-name="Groupe 50" transform="translate(0 0)">
                            <path id="Tracé_48" data-name="Tracé 48" d="M-16.94-.106V8.2c0,.005,0,.005,0,.007V89.042a15.158,15.158,0,0,1-15.141,15.139c-.007,0-.012-.007-.018-.007s-.012.007-.017.007H-46.938c-.009,0-.013-.007-.02-.007s-.011.007-.017.007A15.156,15.156,0,0,1-62.117,89.042V59.33a.283.283,0,0,1,.282-.283A15.156,15.156,0,0,1-46.693,74.186V96.4c.012.031.039.057.039.092a7.134,7.134,0,0,0,7.127,7.126A7.135,7.135,0,0,0-32.4,96.49c0-.036.028-.061.039-.092V8.2s0,0,0-.007A8.431,8.431,0,0,1-24.12-.389h6.9a.278.278,0,0,1,.279.283" transform="translate(62.117 0.389)"/>
                        </g>
                        <g id="Groupe_51" data-name="Groupe 51" transform="translate(52.441 29.716)">
                            <path id="Tracé_49" data-name="Tracé 49" d="M0-22.39V-37.246A15.153,15.153,0,0,1,15.139-52.383h7.41a15.038,15.038,0,0,1,7.165,1.808V-74.313c-.014-.034-.039-.059-.039-.095a7.136,7.136,0,0,0-7.126-7.127,7.135,7.135,0,0,0-7.127,7.127v7.447A15.156,15.156,0,0,1,.283-51.82.283.283,0,0,1,0-52.1V-66.961A15.158,15.158,0,0,1,15.139-82.1H29.959c.007,0,.011.009.018.009s.011-.009.018-.009A15.158,15.158,0,0,1,45.136-66.961v51.112c0,.009.009.013.009.023v8.3a.283.283,0,0,1-.283.283h-6.9a8.07,8.07,0,0,1-6.285-3.095,15.046,15.046,0,0,1-9.128,3.09h-7.41A15.159,15.159,0,0,1,0-22.39m15.422,7.452a7.134,7.134,0,0,0,7.127,7.126,14.489,14.489,0,0,0,8.778-2.968,8.742,8.742,0,0,1-1.609-5.038s0,0,0-.009V-49.922a14.453,14.453,0,0,0-7.165-1.9,7.134,7.134,0,0,0-7.127,7.126Z" transform="translate(0 82.102)"/>
                        </g>
                        <g id="Groupe_52" data-name="Groupe 52" transform="translate(104.882 29.697)">
                            <path id="Tracé_50" data-name="Tracé 50" d="M-.008-24.876c0-.018-.02-.03-.02-.049V-82.614c0-.014.013-.025.016-.039v-8.264A.283.283,0,0,1,.271-91.2h6.9a8.076,8.076,0,0,1,6.264,3.068,15.03,15.03,0,0,1,9.124-3.088H29.97A15.159,15.159,0,0,1,45.111-76.079v51.143s0,0,0,.007v8.3a.283.283,0,0,1-.283.283h-6.9a8.429,8.429,0,0,1-8.245-8.585s0-.005,0-.007V-83.528a7.134,7.134,0,0,0-7.126-7.126,14.49,14.49,0,0,0-8.773,2.964,8.727,8.727,0,0,1,1.631,5.074c0,.02-.018.033-.023.055v57.583c0,.018.023.032.023.052v8.3a.283.283,0,0,1-.283.283h-6.9A8.427,8.427,0,0,1-.008-24.876" transform="translate(0.028 91.22)"/>
                        </g>
                        <g id="Groupe_53" data-name="Groupe 53" transform="translate(157.176 29.72)">
                            <path id="Tracé_51" data-name="Tracé 51" d="M0-22.391V-66.963A15.157,15.157,0,0,1,15.139-82.105c.009,0,.014.009.02.009s.012-.009.018-.009H30A15.158,15.158,0,0,1,45.136-66.963v14.837A15.158,15.158,0,0,1,30-36.987h-7.41a15.054,15.054,0,0,1-7.165-1.807v23.756c.014.032.039.057.039.093a7.136,7.136,0,0,0,7.126,7.126,7.135,7.135,0,0,0,7.127-7.126v-7.447A15.157,15.157,0,0,1,44.854-37.531a.282.282,0,0,1,.282.282v14.856A15.158,15.158,0,0,1,30-7.254H15.177c-.007,0-.011-.007-.018-.007s-.013.007-.02.007A15.154,15.154,0,0,1,0-22.391M15.422-39.455a14.455,14.455,0,0,0,7.165,1.9,7.135,7.135,0,0,0,7.127-7.126V-74.415a7.137,7.137,0,0,0-7.127-7.127,7.136,7.136,0,0,0-7.126,7.127c0,.036-.025.06-.039.092Z" transform="translate(0 82.105)"/>
                        </g>
                        </g>
                    </g>
                </svg>
                <svg @click="isActive = !isActive" v-bind:class="{ icon_is_open: isActive }" class="icon_is_close" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="202.312" height="104.576" viewBox="0 0 202.312 104.576">
                    <defs>
                        <clipPath id="clip-path">
                        <path id="Tracé_52" data-name="Tracé 52" d="M0-39.212H202.312V-143.788H0Z" transform="translate(0 143.788)" fill="none"/>
                        </clipPath>
                    </defs>
                    <g id="Groupe_55" data-name="Groupe 55" transform="translate(0 143.788)">
                        <g id="Groupe_54" data-name="Groupe 54" transform="translate(0 -143.788)" clip-path="url(#clip-path)">
                        <g id="Groupe_50" data-name="Groupe 50" transform="translate(0 0)">
                            <path id="Tracé_48" data-name="Tracé 48" d="M-16.94-.106V8.2c0,.005,0,.005,0,.007V89.042a15.158,15.158,0,0,1-15.141,15.139c-.007,0-.012-.007-.018-.007s-.012.007-.017.007H-46.938c-.009,0-.013-.007-.02-.007s-.011.007-.017.007A15.156,15.156,0,0,1-62.117,89.042V59.33a.283.283,0,0,1,.282-.283A15.156,15.156,0,0,1-46.693,74.186V96.4c.012.031.039.057.039.092a7.134,7.134,0,0,0,7.127,7.126A7.135,7.135,0,0,0-32.4,96.49c0-.036.028-.061.039-.092V8.2s0,0,0-.007A8.431,8.431,0,0,1-24.12-.389h6.9a.278.278,0,0,1,.279.283" transform="translate(62.117 0.389)"/>
                        </g>
                        <g id="Groupe_51" data-name="Groupe 51" transform="translate(52.441 29.716)">
                            <path id="Tracé_49" data-name="Tracé 49" d="M0-22.39V-37.246A15.153,15.153,0,0,1,15.139-52.383h7.41a15.038,15.038,0,0,1,7.165,1.808V-74.313c-.014-.034-.039-.059-.039-.095a7.136,7.136,0,0,0-7.126-7.127,7.135,7.135,0,0,0-7.127,7.127v7.447A15.156,15.156,0,0,1,.283-51.82.283.283,0,0,1,0-52.1V-66.961A15.158,15.158,0,0,1,15.139-82.1H29.959c.007,0,.011.009.018.009s.011-.009.018-.009A15.158,15.158,0,0,1,45.136-66.961v51.112c0,.009.009.013.009.023v8.3a.283.283,0,0,1-.283.283h-6.9a8.07,8.07,0,0,1-6.285-3.095,15.046,15.046,0,0,1-9.128,3.09h-7.41A15.159,15.159,0,0,1,0-22.39m15.422,7.452a7.134,7.134,0,0,0,7.127,7.126,14.489,14.489,0,0,0,8.778-2.968,8.742,8.742,0,0,1-1.609-5.038s0,0,0-.009V-49.922a14.453,14.453,0,0,0-7.165-1.9,7.134,7.134,0,0,0-7.127,7.126Z" transform="translate(0 82.102)"/>
                        </g>
                        <g id="Groupe_52" data-name="Groupe 52" transform="translate(104.882 29.697)">
                            <path id="Tracé_50" data-name="Tracé 50" d="M-.008-24.876c0-.018-.02-.03-.02-.049V-82.614c0-.014.013-.025.016-.039v-8.264A.283.283,0,0,1,.271-91.2h6.9a8.076,8.076,0,0,1,6.264,3.068,15.03,15.03,0,0,1,9.124-3.088H29.97A15.159,15.159,0,0,1,45.111-76.079v51.143s0,0,0,.007v8.3a.283.283,0,0,1-.283.283h-6.9a8.429,8.429,0,0,1-8.245-8.585s0-.005,0-.007V-83.528a7.134,7.134,0,0,0-7.126-7.126,14.49,14.49,0,0,0-8.773,2.964,8.727,8.727,0,0,1,1.631,5.074c0,.02-.018.033-.023.055v57.583c0,.018.023.032.023.052v8.3a.283.283,0,0,1-.283.283h-6.9A8.427,8.427,0,0,1-.008-24.876" transform="translate(0.028 91.22)"/>
                        </g>
                        <g id="Groupe_53" data-name="Groupe 53" transform="translate(157.176 29.72)">
                            <path id="Tracé_51" data-name="Tracé 51" d="M0-22.391V-66.963A15.157,15.157,0,0,1,15.139-82.105c.009,0,.014.009.02.009s.012-.009.018-.009H30A15.158,15.158,0,0,1,45.136-66.963v14.837A15.158,15.158,0,0,1,30-36.987h-7.41a15.054,15.054,0,0,1-7.165-1.807v23.756c.014.032.039.057.039.093a7.136,7.136,0,0,0,7.126,7.126,7.135,7.135,0,0,0,7.127-7.126v-7.447A15.157,15.157,0,0,1,44.854-37.531a.282.282,0,0,1,.282.282v14.856A15.158,15.158,0,0,1,30-7.254H15.177c-.007,0-.011-.007-.018-.007s-.013.007-.02.007A15.154,15.154,0,0,1,0-22.391M15.422-39.455a14.455,14.455,0,0,0,7.165,1.9,7.135,7.135,0,0,0,7.127-7.126V-74.415a7.137,7.137,0,0,0-7.127-7.127,7.136,7.136,0,0,0-7.126,7.127c0,.036-.025.06-.039.092Z" transform="translate(0 82.105)"/>
                        </g>
                        </g>
                    </g>
                </svg>
            </h1>
        </router-link>
        <i @click="isActive = !isActive" class="burger">
            <svg v-bind:class="{ icon_is_close: isActive }" xmlns="http://www.w3.org/2000/svg" width="68.468" height="33.146" viewBox="0 0 68.468 33.146">
                <g id="Groupe_56" data-name="Groupe 56" transform="translate(-1750.395 -68.717)">
                    <line id="Ligne_1" data-name="Ligne 1" x2="68.468" transform="translate(1750.395 69.717)" fill="" stroke="" stroke-miterlimit="10" stroke-width="2"/>
                    <line id="Ligne_2" data-name="Ligne 2" x2="68.468" transform="translate(1750.395 85.29)" fill="" stroke="" stroke-miterlimit="10" stroke-width="2"/>
                    <line id="Ligne_3" data-name="Ligne 3" x2="68.468" transform="translate(1750.395 100.863)" fill="" stroke="" stroke-miterlimit="10" stroke-width="2"/>
                </g>
            </svg>
            <svg v-bind:class="{ icon_is_open: isActive }" class="icon_is_close" xmlns="http://www.w3.org/2000/svg" width="68.468" height="33.146" viewBox="0 0 68.468 33.146">
                <g id="Groupe_56" data-name="Groupe 56" transform="translate(-1750.395 -68.717)">
                    <line id="Ligne_1" data-name="Ligne 1" x2="68.468" transform="translate(1750.395 69.717)" fill="" stroke="" stroke-miterlimit="10" stroke-width="2"/>
                    <line id="Ligne_2" data-name="Ligne 2" x2="68.468" transform="translate(1750.395 85.29)" fill="" stroke="" stroke-miterlimit="10" stroke-width="2"/>
                    <line id="Ligne_3" data-name="Ligne 3" x2="68.468" transform="translate(1750.395 100.863)" fill="" stroke="" stroke-miterlimit="10" stroke-width="2"/>
                </g>
            </svg>
        </i>
    </div>
    <div v-bind:class="{ is_open: isActive }" class="global-nav is_close">
        <div class="global-content">
            <div class="global-item-image">
                <img alt="utopie" class="global-image" :src="image_utopie">
            </div>
            <div @click="isActive = !isActive" class="global-items">
                <router-link class="global-link" style="cursor: not-allowed" to="/">WORK</router-link>
                <router-link class="global-link" to="/about">ABOUT</router-link>
                <router-link class="global-link" style="cursor: not-allowed" to="/">CONTACT</router-link>
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss">
.global-nav{
    position: fixed;
    left: 0; top: 0; right: 0; bottom: 0;
    overflow: hidden;
    height: 100%;
    width: 100%;
    background: #EBEBFF;
    transition: all 150ms ease .1s;
    z-index: 110;
    & .global-content{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        height: 100%;
        width: auto;
        margin: 0 auto;
        & .global-item-image{
            max-height: 528px;
            max-width: 654px;
            & .global-image{
                width: 100%;
                height: 100%;
                object-fit: contain;
                margin: 0 auto;
            }
        }
        & .global-items{
            padding-top: 5rem;
            display: flex;
            flex-direction: column;
            & .global-link{
                margin-left: 3rem;
                font-family: "AméliaDisplayBlack";
                font-size: 170px;
                margin-top: 1rem;
                color: #000;
                text-decoration: none;
                transition: opacity 150ms ease;
                &:hover{
                    opacity: .8;
                }
            }
        }
    }
}
.is_close{
    opacity: 0;
    visibility: hidden;
}
.is_open{
    opacity: 1 !important;
    visibility: visible !important;
}
.icon_is_close{
    display: none;
}
.icon_is_open{
    display: block;
}
.scroll-transition{
    opacity: 0 !important;
    transform: translateY(-5rem) !important;
}
#nav{
    position: fixed;
    transform: translateY(0);
    transition: all 150ms ease;
    top: 50px;
    left: 0;
    right: 0;
    max-width: calc(100% - 112px);
    width: 100%;
    margin: 0 auto;
    z-index: 111;
    opacity: 1;
}
.menu-navigation{
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    & a{
        text-decoration: none;
        color: black;
    }
    & h1.logo{
        font-family: "AméliaDisplayBlack";
        font-size: 152px;
        margin: 0;
    }
    & .burger{
        padding-top: 2px;
        cursor: pointer;
        & svg > *{
            stroke: #fff;
        }
    }
}

</style>

<script>
import image_utopie from "@/assets/img/Utopie.png";
export default{
    /*methods: {
        openMenu(){
           let mymodal = this.$refs.modal
           console.log(mymodal)
           mymodal.classList.toggle("is-open")
        }
    }*/
    data: function () {
        return {
            image_utopie: image_utopie,
            isActive: false,
        }
    }
}

function scrollDetect(){
  var lastScroll = 0;

  window.onscroll = setInterval(function() {
      let currentScroll = document.documentElement.scrollTop || document.body.scrollTop; // Get Current Scroll Value

      if (currentScroll > 0 && lastScroll <= currentScroll){
        lastScroll = currentScroll;
        document.getElementById("nav").classList.add("scroll-transition");
      }else{
        lastScroll = currentScroll;
        document.getElementById("nav").classList.remove("scroll-transition");
      }
  }, 1000);
}
scrollDetect();
</script>