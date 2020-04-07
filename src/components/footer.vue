<template>
    <div class="footerComponent">
        <div class="photoCredits">
            <p>credit for background photo goes to</p>
            <p>Norbert Kundrak on Unsplash</p>
        </div>

        <div class="copyright">
            <p>Oto güneş 2020 &copy;</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "footerComponent"
    
}
</script>

<style scoped>
    p{
        color: white;
        font-size: 1rem;
    }

    .footerComponent{
        cursor: default;
        width: 100%;
        height: 100%;

        padding: 1rem;

        background: black;
    }

    .photoCredits{
        position: absolute;
        width: fit-content;

        display: flex;
        flex-direction: column;

        top: 3rem;
    }

    .copyright{
        position: absolute;

        right: 1rem;

        width: 30rem;
        height: 6rem;

        display: flex;
        align-items: flex-end;
        justify-content: flex-end;
    }

</style>