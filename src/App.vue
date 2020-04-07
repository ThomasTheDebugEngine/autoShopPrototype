<template>
  <div id="app">
    <header class="navbar">
        <navbarComponent/>
    </header>

    <section class="landingSection">
        <div class="mapArea">
            <mapAreaComponent/>
        </div>
        
        <div class="infoArea">
            <infoAreaComponent/>
        </div>
    </section>

    <footer class="footerBar">
        <footerComponent/>
    </footer>
  </div>
</template>

<script>
import navbarComponent from "./components/navbar";
import infoAreaComponent from "./components/infoArea";
import footerComponent from "./components/footer";
import mapAreaComponent from "./components/map";

export default {
    name: 'App',

    components: {
        navbarComponent,
        infoAreaComponent,
        footerComponent,
        mapAreaComponent
    },
}
</script>

<style>
    *{
        box-sizing: border-box;
        margin: 0;
        padding: 0;
        font-size: 62.5%;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }

    #app {
        position: relative;
        height: 100vh; /* make 200 if another section is needed */
    }

    .navbar{
        position: fixed;

        width: 100%;
        height: 8rem;

        z-index: 1;
    }

    .footerBar{
        position: fixed;

        bottom: 0;
        left: 0;

        width: 100%;
        height: 8rem;
    }

    .landingSection{
        width: 100%;
        height: 100vh;

        padding: 9rem 1rem 9rem 1rem;

        display: flex;

        background: url("./assets/suv2.jpg");
        background-position: top;
    }

    .landingSection .mapArea{
        width: 100%;
        height: 100%;
    }

    .landingSection .mapArea:hover{
        cursor: grab;
    }

    .landingSection .infoArea{
        width: 100%;
        height: 100%;

        flex-shrink: 2.5;
    }

    @media only screen and (max-width: 700px) {
        .landingSection{
            flex-direction: column;
        }

        .landingSection .mapArea{
            height: 85%;
        }
    }
    
    @media only screen and (max-width: 500px){
        .landingSection{
            height: 100vh;
            padding-top: 8.2rem;
        }

        .landingSection .mapArea{
            height: 60%;
        }
    }

</style>