<template>
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
</template>

<script>
export default {
    name: "About"
}
</script>

<style scoped>

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

</style>