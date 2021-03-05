<template>
  <header class="l-header" id="header" @scroll="scrollHeader">
        <nav class="nav bd-container" id="navbar">
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
                <button class="nav_button" id="nav-button"  @click="showMenu('nav-button', 'nav-menu')">
                    <i class='bx bx-menu'></i>
                </button>
            </div>
        </nav>
    </header>
</template>

<script>

export default {
    methods: {
        showMenu(toggleId, navId){
    const toggle = document.getElementById(toggleId),
        nav = document.getElementById(navId);
    
    if (toggle && nav) {
        toggle.addEventListener('click', () => {
            nav.classList.toggle('show-menu')
        });
    }
},
        // ==== REMOVE MENU MOBILE ==== 
        linkAction (){
            const navLink = document.querySelectorAll('.nav_link');
            const navMenu = document.getElementById('nav-menu');
            navMenu.classList.remove('show-menu');
        },
        // Changing the color of the navbar on scroll
        scrollHeader(){
            const header = document.getElementById('header');
            if (this.scrollY >= 600) header.classList.add('scroll-header'); else header.classList.remove('scroll-header');
        }
    },
    mounted(){
        
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
/* SHOW MENU */
.show-menu {
    top: var(--header-height);
}

.scroll-header {
    background-color: var(--first-color-lighten);
    box-shadow: 0 2px 4px rgba(0,0,0,.1);
}

.scroll-header .nav_logo, .scroll-header .nav_toggle, .scroll-header .nav_link {
    color: var(--first-color-dark);
}

.scroll-header .nav_menu {
    background-color: var(--first-color-lighten);
}
.nav_button{
    background: inherit;
    color: inherit;
    padding: 0;
    border: none;
    font-size: 1.5rem;
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