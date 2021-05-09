<template>
    <div class="whyeasydetails">
        <img :src="getImgUrl(link)" alt="">
        <p class="header-text sub-header-main">
            {{ subHeaderMain }}
        </p>
        <p class="main-text">
            {{ subHeader }}
        </p>
    </div>
</template>

<script>
export default {
    props: ['link', 'subHeaderMain', 'subHeader'],
    methods: {
        getImgUrl(image) {
            let img = image.split('.')
            img = img[img.length - 1]
            if (img === 'jpg') {
                const images = require.context('../assets/img/', false, /\.jpg$/)
                return images('./' + image)
            } else if (img === 'png') {
                const images = require.context('../assets/img/', false, /\.png$/)
                return images('./' + image)
            } else if (img === 'svg') {
                const images = require.context('../assets/img/', false, /\.svg$/)
                return images('./' + image)
            } else if (img === 'jpeg') {
                const images = require.context('../assets/img/', false, /\.jpeg$/)
                return images('./' + image)
            }
        }

    }
}
</script>

<style lang="scss">
    .whyeasydetails {
        margin-top: 5rem;
        width: 20rem;
        img {
            width: 5rem;
        }

        .sub-header-main {
            font-size: 1.4rem;
            margin-top: 1.5rem;
        }
    }
</style>