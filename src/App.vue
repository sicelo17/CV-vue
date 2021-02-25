<template>
  <router-view/>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500;1,600&display=swap');

 :root {
    --header-height: 3rem;

    /* ==== COLORS ==== */
    --first-color: #3e0e12;
    --first-color-dark: #2f0a0d;
    --text-color: #524748;
    --first-color-light: #7b6f71;
    --first-color-lighten: #fbf9f9;

    /* Font and Typography */
    --body-font: 'Poppins', sans-serif;
    --biggest-font-size: 2.5rem;
    --h1-font-size: 1.5rem;
    --h2-font-size: 1.25rem;
    --h3-font-size: 1.125rem;
    --normal-font-size: .938rem;
    --small-font-size: .813rem;
    --smaller-font-size: .75rem;

    /* Font weight */
    --font-medium: 500;
    --font-semi-bold: 600;
    --font-bold: 700;

    /* Margins */
    --mb-1: .5rem;
    --mb-2: 1rem;
    --mb-3: 1.5rem;
    --mb-4: 2rem;
    --mb-5: 2.5rem;
    --mb-6: 3rem;

    /* z-index */
    --z-normal: 1;
    --z-tooltip: 10;
    --z-fixed: 100;
}

@media screen and (min-width: 768px) {
    :root {
        --biggest-font-size: 4.5rem;
        --h1-font-size: 2.25rem;
        --h2-font-size: 1.5rem;
        --h3-font-size: 1.25rem;
        --normal-font-size: 1rem;
        --small-font-size: .875rem;
        --smaller-font-size: .813rem;
    }
}

/* ==== GLOBAL CSS ==== */
*,::before,::after {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    margin: var(--header-height) 0 0 0;
    font-family: var(--body-font);
    font-size: var(--normal-font-size);
    font-weight: var(--font-medium);
    background-color: var(--first-color-lighten);
    color: var(--text-color);
    line-height: 1.6;
}

h1,h2,h3,ul,p {
    margin: 0;
}

h2,h3 {
    font-weight: var(--font-semi-bold);
}

ul {
    padding: 0;
    list-style: none;
}

a {
    text-decoration: none;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

/* ==== CLASS CSS ==== */
.section {
    padding: 4rem 0 2rem;
}

.section-title, .section-subtitle {
    text-align: center;
}

.section-title {
    font-size: var(--h1-font-size);
    color: var(--first-color);
    margin-bottom: var(--mb-3);
}

.section-subtitle {
    display: block;
    font-size: var(--smaller-font-size);
    font-weight: var(--font-semi-bold);
}

/* ==== LAYOUT ==== */
.bd-container {
    max-width: auto;
    width: calc(100% - 2rem);
    margin-left: var(--mb-2);
    margin-right: var(--mb-2);
}

.bd-grid {
    display: grid;
    gap: 1.5rem;
}

.l-header {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: var(--z-fixed);
    background-color: #000;
}


.button {
    display: inline-block;
    background-color: var(--first-color);
    color: var(--first-color-lighten);
    padding: .75rem 1rem;
    border-radius: .25rem;
    transition: .3s;
}

.button:hover {
    background-color: var(--first-color-dark);
}

.button-light {
    background-color: var(--first-color-light);
}

.button-white {
    background-color: var(--first-color-lighten);
    color: var(--first-color-dark);
}

.button-white:hover {
    background-color: var(--first-color-lighten);
}

.button-link {
    background: none;
    color: var(--first-color-dark);
    padding: 0;
}

.button-link:hover {
    background: none;
}
</style>
