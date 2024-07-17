<template>
    <div class="article">
        <img class="article__img" :src="getImageUrl(article.img_url)" :alt="article.title">
        <div class="article__description">
            <p class="article__description-author">By {{ article.author }}</p>
            <p class="article__description-title"> {{ article.title }}</p>
            <p class="article__description-content"> {{ article.content }}</p>
        </div>

    </div>
</template>

<script setup>
const getImageUrl = (url) => {
    return new URL(url, import.meta.url).href;
}
const { article } = defineProps({
    article: Object
})

</script>

<style  scoped>
.article {
    text-align: left;
    margin: 25px;
    background: white;
}

.article__img {
    border-radius: 5px;
}

.article__description {
    padding: 20px;
    line-height: 1.25rem;
}

.article__description-author {
    font-size: 14px;
    color: var(--color-grayish-blue);
}

.article__description-title {
    font-size: 16px;
}

.article__description-content {
    font-size: 14px;
    color: var(--color-grayish-blue)
}
</style>