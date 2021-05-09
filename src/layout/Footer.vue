<template>
    <div id="footer">
        <div class="left-main">
            <div class="first-col">
                <img src="../assets/img/logo2.svg" alt="" style="color:#fff">
                <div class="icons">
                    <img src="../assets/img/icon-facebook.svg" alt="" style="color:#fff">
                    <img src="../assets/img/icon-pinterest.svg" alt="" style="color:#fff">
                    <img src="../assets/img/icon-twitter.svg" alt="" style="color:#fff">
                    <img src="../assets/img/icon-youtube.svg" alt="" style="color:#fff">
                    <img src="../assets/img/icon-instagram.svg" alt="" style="color:#fff">
                </div>
            </div>
            <div class="second-col">
                <ul>
                    <li class="link">
                        <a href="#">About Us</a>
                    </li>
                    <li class="link">
                        <a href="#">Contact</a>
                    </li>
                    <li class="link">
                        <a href="#">Blog</a>
                    </li>
                </ul>
            </div>
            <div class="third-col">
                <ul>
                    <li class="link">
                        <a href="#">Careers</a>
                    </li>
                    <li class="link">
                        <a href="#">Support</a>
                    </li>
                    <li class="link">
                        <a href="#">Privacy Policy</a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="right-main">
            <div>
                <RequestButton />
            </div>
            <div>
                <p class="copyright">
                    © Easybank. All Rights Reserved
                </p>
            </div>
        </div>
    </div>
</template>

<script>
import RequestButton from "../components/RequestButton";

export default {
    components: {
        RequestButton
    }
}
</script>

<style lang="scss">
    #footer {
        background-color: hsl(233, 26%, 24%);
        padding: 7rem 15rem;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;

        .icons {
            margin-top: 5.5rem;
            display: flex;
            justify-content: space-between;

            img {
                width: 1.4rem;
            }
        }

        .first-col img {
            margin: -1rem 0rem 0rem 0rem;
        }

        .copyright {
            color: #fff;
            margin-top: 3rem;
        }
        
        .left-main {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .right-main {
            text-align: right;
        }

        ul { 
            padding: 0; 
            list-style: none; 
            text-align: left;
            margin-left: 10rem;
        }

        a {
        color: #fff;
        font-weight: 700;
        font-size: 1.3rem;
        text-transform: capitalize;
        text-decoration: none;
        margin-bottom: 1rem;
        display: inline-block;
        padding: 0rem .5rem;
        // position: relative;

        &:hover {
          color: hsl(136, 65%, 51%);
        }
      }

    }
</style>