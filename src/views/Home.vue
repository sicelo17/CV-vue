<template>
    <section class="home" id="home">
            <div class="home_container bd-container b-grid">
                <div class="home_data">
                    <span class="home_greeting">Hi, My name is</span>
                    <h1 class="home_name">Sicelo Sitsha</h1>
                    <span class="home_profession">Web Developer</span>
                    <a download="" href="assets/pdf/Sicelo Sitsha resume.pdf" class="button button-light">Download CV</a>
                </div>

                <div class="home_social" id="home-social" :key="icon" v-for="icon in icons">
                      <a href="#" class="home_social-icon"><i class="{{icon}}"></i></a>
                </div>

                <div class="home_img">
                    <img src="https://images.pexels.com/photos/3568520/pexels-photo-3568520.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" alt="">
                </div>
            </div>
        </section>

    <!-- ==== ABOUT ==== -->
        <section class="about section bd-container" id="about">
            <span class="section-subtitle">My history</span>
            <h2 class="section-title">About Me</h2>

            <div class="about_container bd-grid">
                <div class="about_data bd-grid">
                    <p class="about_description"><span>Hello, I am <br></span> A young and aspiring software developer aged 22 currently studying Computer Science at the National University of Science and Technology popularly known as NUST. I am motivated and inspired to make everyday life easier through the provision of various software in different areas of life</p>

                    <div>
                        <span class="about_number"> 1 </span>
                        <span class="about_achievement">Year of Experience</span>
                    </div>


                    <div>
                        <span class="about_number">5 </span>
                        <span class="about_achievement">Projects Completed</span>
                    </div>
                </div>
                <img src="../assets/img/coffee.jpg" alt="" class="about_img">
            </div>
        </section>

        <!-- ==== QUALIFICATION ==== -->
        <section class="qualification section bd-container">
            <span class="section-subtitle">Experience and Education</span>
            <h2 class="section-title">Qualification</h2>

            <div class="qualification_container bd-grid" id="qualification-area" :key="qualification" v-for="qualification in myJson">
              <div class="qualification_content">
                    <h2 class="qualification-title">
                        <i class="${qualification.icon2}"></i>
                        ${qualification.title}
                    </h2>
                    <div class="bd-grid">
                        <div class="qualification_data">
                            <h3 class="qualification_area">${qualification.area}</h3>
                            <div class="qualification_box">
                                <span class="qualification_work">
                                    <i class="${qualification.icon}"></i>
                                    ${qualification.place}
                                </span>
                                <span class="qualification_work">
                                    <i class="${qualification.work}"></i>
                                    ${qualification.duration}
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ==== SERVICES ==== -->
        <section class="section services bd-container" id="services">
            <span class="section-subtitle">What I offer</span>
            <h2 class="section-title">Services</h2>

            <div class="services_container bd-grid" id="serv">
              <div class="services_data" v-for="service in myJson" :key="service">
                        <i class="${service.icon}"></i>
                        <h3 class="services_title">${service.name}</h3>
                        <p class="services_description">Services that I offer and are very passionate about</p>
                        <a href="#" class="button">Know More</a>
              </div>
            </div>
        </section>

        <!-- ==== PROJECT IN MIND ==== -->
        <section class="project section bd-container">
            <div class="project_container bd-grid">
                <div class="project_data">
                    <i class="bx bx-chat project_icon"></i>

                    <div>
                        <h2 class="project_title">Project in Mind</h2>
                        <p class="project_description">Hire me to carry out the project</p>
                    </div>

                    <div>
                        <a href="#" class="button button-white">Hire Me</a>
                    </div>
                </div>
            </div>
        </section>

</template>


<script>

import json from '../assets/json/constants.json'
export default {
  name: "Home",
  computed: {
    icons() {
      return json.home.map((item) =>{
        return item.icon;
      })
    }
  }
};

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

/* ===== ABOUT ==== */
.about_data {
    text-align: center;
}

.about_description span {
    font-size: var(--h2-font-size);
    font-weight: var(--font-semi-bold);
    color: var(--first-color);
}

.about_number {
    font-size: var(--h1-font-size);
    color: var(--first-color);
    display: block;
}

.about_img {
    justify-self: center;
    width: 450px;
    border-radius: .5rem;
}

/* ==== QUALIFICATION ==== */
.qualification_container {
    row-gap: 2.5rem;
}

.qualification_title {
    font-size: var(--h3-font-size);
    color: var(--first-color);
    margin-bottom: var(--mb-3);
    display: flex;
    align-items: center;
}

.qualification_title-icon {
    font-size: 1.5rem;
    margin-right: var(--mb-1);
}

.qualification_box {
    padding-bottom: 1rem;
    border-bottom: 1px solid #ccc;
}

.qualification_area {
    font-size: var(--normal-font-size);
    color: var(--first-color);
    margin-bottom: var(--mb-1);
    font-weight: var(--font-medium);
}

.qualification_icon, .qualification_work {
    font-size: var(--smaller-font-size);
    color: var(--first-color-light);
}

.qualification_work {
    display: block;
}

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

/* ==== PROJECT IN MIND */
.project_container {
    padding: 1.5rem 1rem;
    background-color: var(--first-color-dark);
    color: var(--first-color-lighten);
    border-radius: .5rem;
    text-align: center;
}

.project_icon, .project_title {
    margin-bottom: var(--mb-1);
}

.project_icon {
    font-size: 3.5rem;
}

.project_title {
    font-size: 1.5rem;
}

.project_description {
    margin-bottom: var(--mb-4);
}

/* MEDIA QUERIES */
@media screen and (min-width: 576px) {
    .home_img img {
        width: 330px;
    }

    .about_container, 
    .qualification_container,
    .services_container {
        grid-template-columns: repeat(2, 1fr);
    }
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
        flex-direction: row;
        align-items: center;
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