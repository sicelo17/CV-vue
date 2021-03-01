<template>
  <footer class="footer">
        <div class="footer_container bd-container">
            <h1 class="footer_title">Sicelo Sitsha</h1>
            <p class="footer_description">I am Sicelo Sitsha and this is my personal portfolio website</p>

            <div class="footer_social">
                <a href="#" class="footer_link"><i class="bx bxl-github contact_icon"></i></a>
                <a href="#" class="footer_link"><i class="bx bxl-linkedin contact_icon"></i></a>
                <a href="#" class="footer_link"><i class="bx bxl-instagram contact_icon"></i></a>
                <a href="#" class="footer_link"><i class="bx bxl-twitter contact_icon"></i></a>
            </div>
            <div class="footer_des">
                <p class="footer_copy">All Rights Reserved &copy; 2021</p>
            </div>

        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
.footer {
    background-color: var(--first-color-dark);
    color: var(--first-color-lighten);
    text-align: center;
}

.footer_container {
    padding: 3rem 0;
}

.footer_title {
    font-size: var(--h2-font-size);
    margin-bottom: var(--mb-1);
    font-weight: var(--font-semi-bold);
}

.footer_description {
    margin-bottom: var(--mb-3);
}

.footer_social {
    margin-bottom: var(--mb-6);
}

.footer_link {
    font-size: 1.6rem;
    color: var(--first-color-lighten);
    
    margin: 0 var(--mb-1);
    transition: .3s;
}

.footer_link:hover {
    background-color: var(--first-color-light);
}

</style>