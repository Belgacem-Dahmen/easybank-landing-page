<template>
    <div class="navbar">
        <img class="navbar-logo" src="../assets//images/logo.svg" alt="">
        <div class=" hidden-on-mobile navbar-links">
            <ul>
                <li> Home</li>
                <li>About</li>
                <li>Contact</li>
                <li>Blog</li>
                <li>Careers</li>
            </ul>

        </div>
        <Primaybtn :hiddenOnMobile=true text="Request Invite" />
        <img class="hidden-on-desktop" src="../assets/images/icon-hamburger.svg" alt="">
    </div>
</template>

<script setup>
import Primaybtn from './Primaybtn.vue';
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

@media screen and (min-width : 376px) {
    .navbar {
        padding: 20px 100px;
    }

}
</style>