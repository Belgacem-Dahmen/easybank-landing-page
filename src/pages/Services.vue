<script setup>
import { ref } from 'vue';
import Service from '../components/Service.vue';
const services = ref([
    {
        "id": 1,
        "url_img": "link_to_online_banking_image",
        "title": "Online Banking",
        "description": "Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world."
    },
    {
        "id": 2,
        "url_img": "link_to_simple_budgeting_image",
        "title": "Simple Budgeting",
        "description": "See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits."
    },
    {
        "id": 3,
        "url_img": "link_to_fast_onboarding_image",
        "title": "Fast Onboarding",
        "description": "We don’t do branches. Open your account in minutes online and start taking control of your finances right away."
    },
    {
        "id": 4,
        "url_img": "link_to_open_api_image",
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

        <div v-for="service in services" :key="service.id">
            <Service :service="service"/>
        </div>


    </div>
</template>


<style  scoped>
.services {
    margin-top: 150px;
    text-align: center;
    padding: 20px;
}


.services-title {
    font-weight: 500;
    line-height: 2.25rem;
}

.services-description {
    color: var(--color-grayish-blue);
    font-size: 15px;

}
</style>