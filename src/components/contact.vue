
<template>
    <div class="contact-form">
        <h1>Contact me</h1>
        <div>
            <a target="_blank" href="mailto:jeanne.chevallier@yahoo.fr?subject=Contact%20from%20lajanecy&body=I%20would%20like%20to%20contact%20you...">
                <button>EMAIL</button>
            </a>
            <a target="_blank" href="https://www.instagram.com/lajanecy/">
                <button>INSTAGRAM</button>
            </a>
            <a href="tel:+33698555357">
                <button>PHONE</button>
            </a>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@import '@/assets/variables.scss';
@import '@/assets/global.scss';
.contact-form{
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: center;
    align-items: center;
    & h1{
        font-size: 190px;
        font-family: "AméliaDisplay";
        letter-spacing: -5px;
        text-transform: uppercase;
        line-height: 1;
        margin: 0;
        margin-bottom: 3rem;
    }
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
        margin-inline: 1rem;
        transition: 0.25s ease;
    }
}
</style>