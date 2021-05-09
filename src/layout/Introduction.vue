<template>
    <div id="introduction">
        <div class="left-div text-left">
            <p class="header-text head">Next generation digital banking</p>
            <p class="main-text second-para">
                Take your financial life online. Your Easybank 
                account will be a one-stop-shop for spending, 
                saving, budgeting, investing, and much more.
            </p>
            <RequestButton />
        </div>
        <div class="right-div">
            <img src="../assets/img/bg-intro-desktop.svg" alt="" class="image-1">
            <img src="../assets/img/image-mockups.png" alt="" class="image-2">
            <img src="../assets/img/bg-intro-mobile.svg" alt="" class="image-3">
        </div>
    </div>
</template>

<script>
import RequestButton from "../components/RequestButton";

export default {
    components: {
        RequestButton,
    }
}
</script>

<style lang="scss">
    #introduction {
        display: flex;
        justify-content: space-between;
        background-color: hsl(0, 0%, 98%);
        height: auto;

        .image-3 {
            display: none;
        }

        .second-para {
            margin-bottom: 3.5rem;
        }

        .left-div, .right-div {
            width: 50vw;
        }

        .right-div {
            // background-color: red;
        }

        .image-1, .image-2, .image-3 {
            position: absolute;
        }
            
        .image-1 {
            top: -18rem;
            right: -20rem;
            width: 90rem;
            // width: 60vw;
            z-index: 9;
        }

        .image-2 {
            width: 62rem;
            top: -9rem;
            right: -11rem;
            z-index: 99
        }

        .head {
            font-size: 2.8rem;
        }

        .left-div {
            padding: 15rem 5rem 18rem 15rem
        }
    }
</style>