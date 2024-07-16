<template>
    <div class="intro">
        <div class="intro-imgs">
            <img class="intro-mokup" src="../assets/images/image-mockups.png" alt="">
        </div>
        <div class="intro-text">
            <h1 class="intro-text-title">
                Next generation digital banking
            </h1>
            <p class="intro-text-description">
                Take your financial life online. Your Easybank account will be a one-stop-shop
                for spending, saving, budgeting, investing, and much more.
            </p>


            <PrimaryBtn :hiddenOnMobile=false text="Request Invite" />
        </div>
    </div>
</template>

<script setup>
import PrimaryBtn from '../components/PrimaryBtn.vue';
</script>

<style scoped>
.intro {
    display: flex;
    flex-direction: column;
    position: relative;
}

.intro-imgs {
    position: absolute;
    min-height: 500px;
    top: -20%;
    z-index: -2;
    background-image: url(../assets/images/bg-intro-mobile.svg);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    text-align: center;
    padding: 0 20px;

}

.intro-text {
    margin-top: 350px;
    text-align: center;
}

.intro-text-title {
    font-weight: var(--font-weight-regular);
    font-size: 2.5rem;
    line-height: 2.5rem;

}

.intro-text-description {
    padding: 10px 20px;
    font-size: 15px;
    text-align: justify;
    color: var(--color-grayish-blue);
}

@media screen and (min-width:376px) {
    .intro {
        
        flex-direction: row;

    }

    .intro-imgs {
        position: absolute;
        background-position: bottom;
        right: -10%;
        top: -30%;
    }

    .intro-text {
        margin-top: 150px;
        text-align: left;
        max-width: 500px;
        align-self: center;
        justify-self: flex-start;
        padding-left: 100px;
    }


}
</style>