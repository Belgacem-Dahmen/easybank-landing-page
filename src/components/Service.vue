<template>
    <article class="service">

        <img :src="service.url_img" alt="">
        <p class="service-title">{{ service.title }}</p>


        <p class="service-description"> {{ service.description }}</p>
    </article>
</template>

<script setup>
const { service } = defineProps({
    service: Object
})
</script>

<style scoped>
.service {
    display: flex;
    flex-direction: column;
    gap: 10px;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 15px;
}

.service-description {
    color: var(--color-grayish-blue);
    font-size: 14px;
}

@media screen and (max-width:376px) {
    .service {
        display: flex;
        flex-direction: column;
        gap: 10px;
        align-items: center;
        justify-content: center;
        margin-top: 15px;
    }
}
</style>