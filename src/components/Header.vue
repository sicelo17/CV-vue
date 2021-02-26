<template>
  <header class="l-header" id="header">
        <nav class="nav bd-container">
            <a href="#" class="nav_logo">Sicelo Sitsha</a>

            <div class="nav_menu" id="nav-menu">
                <ul class="nav_list">
                    <li class="nav_item"><a href="#home" class="nav_link active-link">Home</a></li>
                    <li class="nav_item"><a href="#about" class="nav_link">About</a></li>
                    <li class="nav_item"><a href="#services" class="nav_link">Services</a></li>
                    <li class="nav_item"><a href="#portfolio" class="nav_link">Portfolio</a></li>
                    <li class="nav_item"><a href="#contact" class="nav_link">Contact</a></li>
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

}
</script>

<style>
.nav {
    height: var(--header-height);
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav_item {
    margin-bottom: var(--mb-3);
}

.nav_link {
    color: var(--first-color-lighten);
    transition: .3s;
}

.nav_link:hover {
    color: var(--first-color-light);
}

.nav_logo, .nav_toggle {
    color: var(--first-color-lighten);
}

.nav_toggle {
    font-size: 1.3rem;
    cursor: pointer;
}

</style>