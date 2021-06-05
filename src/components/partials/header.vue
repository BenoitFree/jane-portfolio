<template>
    <div id="nav" class="menu-navigation">
        <a href="/about"><h1 class="logo">JANE</h1></a>
        <i class="burger">
            <svg xmlns="http://www.w3.org/2000/svg" width="58.285" height="27.514" viewBox="0 0 58.285 27.514">
                <g id="Groupe_12" data-name="Groupe 12" transform="translate(-1750.395 -69.217)">
                    <line id="Ligne_1" data-name="Ligne 1" x2="58.285" transform="translate(1750.395 69.717)" fill="none" stroke="#161615" stroke-miterlimit="10" stroke-width="1"/>
                    <line id="Ligne_2" data-name="Ligne 2" x2="58.285" transform="translate(1750.395 82.974)" fill="none" stroke="#161615" stroke-miterlimit="10" stroke-width="1"/>
                    <line id="Ligne_3" data-name="Ligne 3" x2="58.285" transform="translate(1750.395 96.23)" fill="none" stroke="#161615" stroke-miterlimit="10" stroke-width="1"/>
                </g>
            </svg>
        </i>
    </div>
</template>

<style lang="scss">
#nav{
    position: fixed;
    top: 74px;
    left: 0;
    right: 0;
    max-width: calc(100% - 112px);
    width: 100%;
    margin: 0 auto;
    z-index: 111;
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
        margin-left: 56px;
    }
    & .burger{
        cursor: pointer;
    }
}

</style>