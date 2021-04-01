<template>
    <header class="l-header" id="header">
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
                <button class="nav_button" id="nav-button" @click="toggleMenu">
                    <i class='bx bx-menu'></i>
                </button>
            </div>
        </nav>
    </header>
</template>

<script>

export default {
    methods: {
        toggleMenu() {
            let menuBox = document.getElementById('nav-menu'); 
            // if is menuBox displayed, hide it   
            if(menuBox.style.top == "3rem") { 
                menuBox.style.top = "-100%";
            }
            // if is menuBox hidden, display it
            else { 
                menuBox.style.top = "3rem";
            }
        },
        scrollHeader(){
            
            console.log("scrolled")
        }
        },
        mounted(){
            window.addEventListener("scroll", this.scrollHeader)
        },
        unmounted(){
            window.removeEventListener("scroll", this.scrollHeader)
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
    .nav_list {
        display: flex;
        flex-direction: column;
    }
}
</style>