<template>
         <!-- ==== QUALIFICATION ==== -->
        <section class="qualification section bd-container">
            <span class="section-subtitle">Experience and Education</span>
            <h2 class="section-title">Qualification</h2>

            <div class="qualification_container bd-grid" id="qualification-area" :key="qualification" v-for="qualification in qualifications">
              <div class="qualification_content">
                    <h2 class="qualification-title">
                        <i class="{{qualification.icon2}}"></i>
                        {{qualification.title}}
                    </h2>
                    <div class="bd-grid">
                        <div class="qualification_data">
                            <h3 class="qualification_area">{{qualification.area}}</h3>
                            <div class="qualification_box">
                                <span class="qualification_work">
                                    <i class="{{qualification.icon}}"></i>
                                    {{qualification.place}}
                                </span>
                                <span class="qualification_work">
                                    <i class="{{qualification.work}}"></i>
                                    {{qualification.duration}}
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

</template>

<script>
export default {
    name: "Qualification",
    data(){
        return{
            qualifications: []
        }
    },
    mounted(){
         fetch('http://localhost:3000/qualification')
            .then(res => res.json())
            .then(data => this.qualifications = data)
            .catch(err => console.log(err))
            
    }
}
</script>

<style scoped>
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
</style>