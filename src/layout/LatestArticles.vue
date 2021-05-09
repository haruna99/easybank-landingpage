<template>
    <div id="latest-article" class="text-left">
        <p class="header-text head">
            Latest Articles
        </p>
        <div class="cards">
            <div class="first">
                <LatestArticlesCard :image="latestArticle[0].image" :author="latestArticle[0].author" :headerText="latestArticle[0].headerText" :mainText="latestArticle[0].mainText" />
            </div>
            <div class="second">
                <LatestArticlesCard :image="latestArticle[1].image" :author="latestArticle[1].author" :headerText="latestArticle[1].headerText" :mainText="latestArticle[1].mainText" />
            </div>
            <div class="third">
                <LatestArticlesCard :image="latestArticle[2].image" :author="latestArticle[2].author" :headerText="latestArticle[2].headerText" :mainText="latestArticle[2].mainText" />
            </div>
            <div class="fourth">
                <LatestArticlesCard :image="latestArticle[3].image" :author="latestArticle[3].author" :headerText="latestArticle[3].headerText" :mainText="latestArticle[3].mainText" />
            </div>
        </div>
    </div>
</template>

<script>
import LatestArticlesCard from "../components/LatestArticlesCard";

export default {
    data() {
        return {
            latestArticle: [
                {image: 'image-currency.jpg', author: 'By Claire Robinson', headerText: 'Receive money in any currency with no fees', mainText: 'The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …'},
                {image: 'image-restaurant.jpg', author: 'By Wilson Hutton', headerText: 'Treat yourself without worrying about money', mainText: 'Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …'},
                {image: 'image-plane.jpg', author: 'By Wilson Hutton', headerText: 'Take your Easybank card wherever you go', mainText: 'We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …'},
                {image: 'image-confetti.jpg', author: 'By Claire Robinson', headerText: 'Our invite-only Beta accounts are now live!', mainText: 'After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ...'},
            ]
        }
    },
    components: {
        LatestArticlesCard,
    }
}
</script>

<style lang="scss">
    #latest-article {
        background-color: hsl(0, 0%, 98%);
        padding: 7rem 15rem;

        .head {
            font-size: 1.8rem;
            margin-bottom: 2.5rem;
        }

        .cards {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        
    }
</style>