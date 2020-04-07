<template>
    <div class="infoAreaComponent">
        <div class="address">
            <h1>Adres</h1>
            <p>
                Oto güneş
                Alt. san Cad No: 12/A <br> 
                Efeler, Aydın
            </p>
            <!-- this breaks when the address is too long (shouldn't be a problem)-->
        </div>

        <hr>

        <div class="phone">
            <h1>Telefon</h1>
            <br>
            <p>
                (+090) 549 124 56 87
            </p>
        </div>

        <hr>

        <div class="extraInfo">
            <h1>Saatler</h1>
            <br>
            <p>we work from 08:00 to 17:00 every weekday</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "infoAreaComponent"   
}
</script>

<style scoped>
    h1{
        font-size: 4rem;
        color: #cfcfcf;
    }

    p{
        font-size: 2rem;
        color: #cfcfcf;
    }

    hr{
        border: 3px solid black; /* maybe change it if its bad (good reference tho) */
    }

    .infoAreaComponent{
        width: 100%;
        height: 100%;
        cursor: default;

        background: rgba(43, 43, 43, 0.7);

        display: flex;
        flex-direction: column;

        border-top-right-radius: 2rem;
        border-bottom-right-radius: 2rem;
    }

    .address{
        box-sizing: border-box;
        width: 100%;
        height: 100%;

        padding: 1rem;

        /* background: purple; */
        display: flex;
        flex-direction: column;
    }

    .phone{
        width: 100%;
        height: 100%;

        padding: 1rem;
    }

    .extraInfo{
        width: 100%;
        height: 100%;

        padding: 1rem;

        /* background: slateblue; */
    }

    @media only screen and (max-width: 700px) {
        .infoAreaComponent{
            flex-direction: row;
            border-radius: 0;
        }

        .address{
            padding: 0;
        }

        h1{
            font-size: 3rem;
        }
    }

    @media only screen and (max-width: 500px){
        .infoAreaComponent{
            flex-direction: column;
        }
    }

</style>