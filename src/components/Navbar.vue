<template>
    <div class="navbar">
        <img class="navbar-logo" src="../assets//images/logo.svg" alt="">
        <div class=" hidden-on-mobile navbar-links">
            <ul class="navbar__list">
                <li class="navbar__list-item"> Home</li>
                <li class="navbar__list-item">About</li>
                <li class="navbar__list-item">Contact</li>
                <li class="navbar__list-item">Blog</li>
                <li class="navbar__list-item">Careers</li>
            </ul>

        </div>
        <PrimaryBtn :hiddenOnMobile=true text="Request Invite" />
        <img class="hidden-on-desktop" src="../assets/images/icon-hamburger.svg" alt="">
    </div>
</template>

<script setup>
import PrimaryBtn from './PrimaryBtn.vue';
</script>

<style scoped>
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: var(--color-white);
    color: var(--color-grayish-blue);
    font-size: 1rem;
    padding: 20px;
}

.navbar-links ul {
    display: flex;
    gap: 25px;
    list-style: none;
}

.navbar__list-item:hover {
    cursor: pointer;
   border-bottom: 1px solid transparent;
    border-image: linear-gradient(to left, var(--color-bright-cyan), var(--color-lime-green));
    border-image-slice: 1;
}

@media screen and (min-width : 376px) {
    .navbar {
        padding: 20px 100px;
    }

}
</style>