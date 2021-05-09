<template>
    <div id="whyeasy" class="text-left">
        <p class="header-text head">
            Why choose Easybank?
        </p>
        <p class="main-text">
            We leverage Open Banking to turn your bank 
            account into your financial hub. Control your 
            finances like never before.
        </p>
        <div class="easy-details">
            <div class="first">
                <WhyEasyDetails :link="easyData[0].link" :subHeaderMain="easyData[0].subHeaderMain" :subHeader="easyData[0].subHeader" />
            </div>
            <div class="second">
                <WhyEasyDetails :link="easyData[1].link" :subHeaderMain="easyData[1].subHeaderMain" :subHeader="easyData[1].subHeader" />
            </div>
            <div class="third">
                <WhyEasyDetails :link="easyData[2].link" :subHeaderMain="easyData[2].subHeaderMain" :subHeader="easyData[2].subHeader" />
            </div>
            <div class="fourth">
                <WhyEasyDetails :link="easyData[3].link" :subHeaderMain="easyData[3].subHeaderMain" :subHeader="easyData[3].subHeader" />
            </div>
        </div>
    </div>
</template>

<script>
import WhyEasyDetails from "../components/WhyEasyDetails";

export default {
    data() {
        return {
            easyData: [
                {link: 'icon-online.svg', subHeaderMain: 'Online Banking', subHeader: 'Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.'},
                {link: 'icon-budgeting.svg', subHeaderMain: 'Simple Budgeting', subHeader: 'See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits.'},
                {link: 'icon-onboarding.svg', subHeaderMain: 'Fast Onboarding', subHeader: 'We don’t do branches. Open your account in minutes online and start taking control of your finances right away.'},
                {link: 'icon-api.svg', subHeaderMain: 'Open API', subHeader: 'Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.'},
            ],
        }
    },
    components: {
        WhyEasyDetails,
    }
}
</script>

<style lang="scss">
    #whyeasy {
        padding: 7rem 15rem;
        background-color: hsl(220, 16%, 96%);

        .head {
            font-size: 1.8rem;
        }

        .easy-details {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        
    }
</style>