<template>
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
export default {
    name: "Project"
}
</script>

<style scoped>
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
</style>