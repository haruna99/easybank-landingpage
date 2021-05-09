<template>
  <v-card
    class="latest-articles-card"
  >

    <v-img
      height="160"
      :src="getImgUrl(image)"
    ></v-img>

    <v-card-title>
        <p class="author mr-4">
            <i>
                {{ author}}:
            </i>
        </p>
        <p class="header-text author-maintext">
            {{ headerText }}
        </p>
        <p class="main-text">
            {{ mainText }} 
        </p>
    </v-card-title>

    <v-card-text>
      
    </v-card-text>

    </v-card>
</template>

<script>
export default {
    props: ['image', 'author', 'headerText', 'mainText'],
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
    .latest-articles-card {
        margin-bottom: 3.5rem;
        width: 20rem;
        cursor: pointer;
        &:hover {
            transform: scale(1.05);
            transition: .3s all ease-in-out;
            .author-maintext {
                color: hsl(136, 65%, 51%);
            }
        }
        .author {
            font-size: 1rem;
        }
    }
</style>