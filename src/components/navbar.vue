<template>
    <div class="navBarComponent">
        <div class="companyLogo"></div>
        <div class="navButtons">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Information</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "navbarComponent"
}
</script>

<style scoped>

    .navBarComponent{
        width: 100%;
        height: 100%;

        display: flex;
    }

    .companyLogo{
        height: 100%;
        min-width: 20rem;

        background: yellow;
    }

    .navButtons{
        height: 100%;
        width: 100%;

        background: #333333;
        display: flex;
        justify-content: flex-end;

        padding-right: 5rem;   
    }

    .navButtons ul{
        list-style: none;

        width: fit-content;
        
        display: flex;
        justify-content: center;
        
        font-size: 8rem;
    }

    .navButtons ul li{
        margin-left: 4rem;

        display: inline-block;
        align-items: center;
        justify-content: center;
    }

    .navButtons ul li:hover{
        cursor: pointer;
        color: #f2f2f2;
    }

    .navButtons ul li a{
        text-decoration: none;
        color: #cfcfcf;
    }

    .navButtons ul li a:hover{
        color: #f2f2f2;
    }

    .navButtons ul li a::after{
        position: relative;

        bottom: -1.4rem;

        content: "";
        display: block;

        width: 0%;
        height: 5px;

        background: #d4d4d4;
        transition: ease-in-out 350ms;
    }

    .navButtons ul li a:hover::after{
        width: 100%;
    }

    @media only screen and (max-width: 700px) {
        .companyLogo{
            min-width: 10rem;
        }
    }

    @media only screen and (max-width: 500px) {
        .companyLogo{
            display: none;
        }

        .navButtons{
            padding-right: 3rem;
        }
    }

</style>