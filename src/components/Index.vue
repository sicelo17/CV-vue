<template>
  <section class="home" id="home">
            <div class="home_container bd-container b-grid">
                <div class="home_data">
                    <span class="home_greeting">Hi, My name is</span>
                    <h1 class="home_name">Sicelo Sitsha</h1>
                    <span class="home_profession">Web Developer</span>
                    <a download="" href="assets/pdf/Sicelo Sitsha resume.pdf" class="button button-light">Download CV</a>
                </div>

                <div class="home_social" id="home-social" :key="item" v-for="item in index">
                      <a href="#" class="home_social-icon"><i :class="item.icon"></i></a>
                </div>

                <div class="home_img">
                    <img src="https://images.pexels.com/photos/3568520/pexels-photo-3568520.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" alt="">
                </div>
            </div>
        </section>

</template>

<script>
import constants from "../../src/assets/json/constants.json";

export default {
    name: "Index",
    data(){
        return {
            index: constants.index
        }
    },
    created(){
        console.log(this.index)
    }
}
</script>

<style scoped>
.home {
    background: #000;
    overflow: hidden;
}

.home_container {
    position: relative;
    height: 90vh;
    grid-template-rows: repeat(2, max-content);
    align-content: space-around;
    row-gap: 2rem;
    margin-top: var(--header-height);
}

.home_data {
    border-left: 4px solid var(--first-color-lighten);
    color: var(--first-color-lighten);
    padding-left: 1.5rem;
    z-index: var(--z-tooltip);
    margin-bottom: 5rem;
}

.home_name {
    font-size: var(--biggest-font-size);
}

.home_greeting, .home_profession {
    display: block;
    font-weight: var(--font-bond);
}

.home_greeting {
    font-size: .813rem;
}

.home_profession {
    font-size: .938rem;
    margin-bottom: var(--mb-3);
}

.home_img {
    position: absolute;
    right: 0;
    bottom: 4rem;
}

.home_img img {
    width: 200px;
}

.home_social {
    display: flex;
    flex-direction: column;
}

.home_social-icon {
    width: max-content;
    font-size: 1.3rem;
    margin-bottom: var(--mb-3);
    color: var(--first-color-lighten);
}

.home_social-icon:hover {
    color: var(--first-color-light);
}


@media screen and (min-width: 768px) {

    .home_container {
        height: 100vh;
        grid-template-rows: max-content .5fr;
        align-content: flex-end;
    }

    .home_greeting {
        font-size: 1.25rem;
    }

    .home_profession {
        font-size: 2rem;
    }

    .home_social {
        display: inline-block;
    }

    .home_social-icon {
        margin-right: var(--mb-4);
        margin-bottom: 0;
        font-size: 2rem;
    }

    .home_img img {
        width: 400px;
    }

    .home_data {
        padding-top: 4rem;
    }

}

</style>