<template>
    <div :class="{ 'navbar-btn': true, 'hidden-on-mobile': hiddenOnMobile }">
        <button>
            {{ text }}
        </button>
    </div>
</template>

<script setup>

const { hiddenOnMobile, text } = defineProps({
    hiddenOnMobile: Boolean,
    text: String
})
</script>

<style scoped>
button {
    background-image: linear-gradient(to left, var(--color-bright-cyan), var(--color-lime-green));
    border-radius: 25px;
    border: 0;
    padding: 10px 25px;
    color: var(--color-white);
    font-size: 14px;
}
</style>