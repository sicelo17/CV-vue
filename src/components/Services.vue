<template>
    <section class="section services bd-container" id="services">
            <span class="section-subtitle">What I offer</span>
            <h2 class="section-title">Services</h2>

            <div class="services_container bd-grid" id="serv">
              <div class="services_data" v-for="service in services" :key="service">
                        <i :class="service.icon"></i>
                        <h3 class="services_title">{{service.name}}</h3>
                        <p class="services_description">Services that I offer and are very passionate about</p>
                        <a href="#" class="button">Know More</a>
              </div>
            </div>
        </section>
</template>

<script>

import constants from "../../src/assets/json/constants.json";
export default {
    data(){
        return{
            services: constants.serviceData
        }
    },
    created(){
        console.log(this.services)
    }
       
}
</script>

<style scoped>
/* ====SERVICES ==== */
.services_data {
    padding: 3rem 1rem;
    background-color: #fff;
    border-radius: .5rem;
    text-align: center;
    transition: .4s;
    box-shadow: 0 4px 6px rgba(174, 190, 205, .3);
}

.services_icon, .services_title {
    margin-bottom: var(--mb-2);
    color: var(--first-color);
}

.services_icon {
    font-size: 3rem;
}

.services_title {
    font-size: var(--h3-font-size);
}

.services_description {
    margin-bottom: var(--mb-4);
}

.services_data:hover {
    transform: translateY(-.5rem);
    box-shadow: 0 6px 8px rgba(174, 190, 205, .4);
}
</style>