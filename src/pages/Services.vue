<script setup>
import { ref } from 'vue';
import Service from '../components/Service.vue';
const services = ref([
    {
        "id": 1,
        "url_img": "src/assets/images/icon-online.svg",
        "title": "Online Banking",
        "description": "Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world."
    },
    {
        "id": 2,
        "url_img": "src/assets/images/icon-budgeting.svg",
        "title": "Simple Budgeting",
        "description": "See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits."
    },
    {
        "id": 3,
        "url_img": "src/assets/images/icon-onboarding.svg",
        "title": "Fast Onboarding",
        "description": "We don’t do branches. Open your account in minutes online and start taking control of your finances right away."
    },
    {
        "id": 4,
        "url_img": "src/assets/images/icon-api.svg",
        "title": "Open API",
        "description": "Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier."
    }
]);

</script>

<template>
    <div class="services">
        <h1 class="services-title">Why choose Easybank?</h1>
        <p class="services-description">We leverage Open Banking to turn your bank account into your financial hub. Control
            your finances like never before.</p>

        <div class="services-container">
            <div v-for="service in services" :key="service.id">
                <Service :service="service" />
            </div>
        </div>

    </div>
</template>


<style  scoped>
.services {
    margin-top: 150px;
    text-align: center;
    padding: 20px;
    background-color: var(---color-light-grayish-blue);
}


.services-title {
    font-weight: 500;
    line-height: 2.25rem;
}

.services-description {
    color: var(--color-grayish-blue);
    font-size: 15px;

}

@media screen and (min-width: 376px) {
    .services {
        margin-top: 350px;
        text-align: left;
        padding: 0 100px;
    }

    .services-container {

        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 25px;
    }
}

/* New styles for tablets */
@media screen and (max-width: 1024px) {
    .services-container {
        grid-template-columns: repeat(2, 1fr);
    }
}
</style>