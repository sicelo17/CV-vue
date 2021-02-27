<template>
  <header class="l-header" id="header">
        <nav class="nav bd-container">
            <a href="#" class="nav_logo">Sicelo Sitsha</a>

            <div class="nav_menu" id="nav-menu">
                <ul class="nav_list">
                    <router-link class="nav_item" to="/">Home</router-link>
                    <router-link class="nav_item" to="/">About</router-link>
                    <router-link class="nav_item" to="/">Services</router-link>
                    <router-link class="nav_item" to="/portfolio">Portfolio</router-link>
                    <router-link class="nav_item" to="/contact">Contact</router-link>
                </ul>
            </div>

            <div class="nav_toggle" id="nav-toggle">
                <i class='bx bx-menu'></i>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    methods: {
        
    }
}
</script>

<style scoped>

.nav {
    height: 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav_item {
    margin-bottom: var(--mb-3);
    padding-top: var(--mb-2);
}

.nav_link,.nav_item:visited {
    color: var(--first-color-lighten);
    transition: .3s;
}

.nav_link:hover, .nav_item:visited:hover {
    color: var(--first-color-light);
}

.nav_logo, .nav_toggle {
    color: var(--first-color-lighten);
}

.nav_toggle {
    font-size: 1.3rem;
    cursor: pointer;
}
@media screen and (max-width: 768px){
    .nav_menu {
        position: fixed;
        top: -100%;
        left: 0;
        width: 100%;
        padding-top: 1.5rem;
        text-align: center;
        background-color: #000;
        transition: .4s;
        box-shadow: 0 2px 4px rgba(0,0,0,.1);
        border-radius: 0 0 1rem 1rem;
    }
}
</style>