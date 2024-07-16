<template>
    <div class="articles">
        <h1 class="article-header">Latest Articles</h1>
        <div class="articles-container">
            <div v-for="article in articles" :key="article.id">
                <Article :article=article />
            </div>
        </div>
    </div>
</template>

<script setup>
import Article from '../components/Article.vue';

const articles =

    [
        {
            "id": 1,
            "author": "Claire Robinson",
            "title": "Receive money in any currency with no fees",
            "content": "The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …",
            "img_url": "src/assets/images/image-currency.jpg"
        },
        {
            "id": 2,
            "author": "Wilson Hutton",
            "title": "Treat yourself without worrying about money",
            "content": "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …",
            "img_url": "src/assets/images/image-restaurant.jpg"
        },
        {
            "id": 3,
            "author": "Wilson Hutton",
            "title": "Take your Easybank card wherever you go",
            "content": "We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …",
            "img_url": "src/assets/images/image-plane.jpg"
        },
        {
            "id": 4,
            "author": "Claire Robinson",
            "title": "Our invite-only Beta accounts are now live!",
            "content": "After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ...",
            "img_url": "src/assets/images/image-confetti.jpg"
        }
    ]




</script>

<style scoped>
.article-header{
        padding-left: 25px;
    }
@media screen and (min-width: 376px) {
    .articles {
        margin-top: 150px;
        text-align: left;
        padding: 0 100px;
    }
    

    .articles-container {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 25px;
    }
}
</style>