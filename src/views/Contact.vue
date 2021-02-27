<template>
  <section class="contact section bd-container" id="contact">
            <span class="section-subtitle">Get in Touch</span>
            <h2 class="section-title">Contact Me</h2>

            <div class="contact_container bd-grid">
                <div class="contact_content bd-grid">
                    <div class="contact_box">
                        <i class="bx bx-home contact_icon"></i>
                        <h3 class="contact_title">Location</h3>
                        <span class="contact_description">Gweru - Zimbabwe</span>
                    </div>

                    <div class="contact_box">
                        <i class="bx bx-phone contact_icon"></i>
                        <h3 class="contact_title">Phone</h3>
                        <span class="contact_description">+263 78 493 9154</span>
                    </div>

                    <div class="contact_box">
                        <i class="bx bx-envelope contact_icon"></i>
                        <h3 class="contact_title">Email</h3>
                        <span class="contact_description">sicelositsha@yahoo.com</span>
                    </div>

                    <div class="contact_box">
                        <i class="bx bx-home contact_icon"></i>
                        <h3 class="contact_title">Chat</h3>
                        <div id="contact-info" :key="contact" v-for="contact in contacts">
                            <a href="#" class="contact_social"><i class="{{contact.icon}}"></i></a>
                        </div>
                    </div>
                </div>

                <form action="" class="contact_form">
                    <div class="contact_inputs">
                        <input type="text" placeholder="Name" class="contact_input">
                        <input type="email" placeholder="Email" class="contact_input">
                    </div>

                    <div class="contact_inputs">
                        <input type="text" placeholder="Project" class="contact_input">
                        <input type="number" placeholder="Number" class="contact_input">
                    </div>

                    <textarea name="" id="" placeholder="Message" cols="30" rows="10" class="contact_input"></textarea>
                    <input type="submit" value="Send Message" class="button contact_button">
                </form>
            </div>
            </section>
</template>

<script>
export default {

    data(){
        return{
            contacts:[]
        }
    },
 mounted() {
     
        fetch('http://localhost:3000/contacts')
            .then(res => res.json())
            .then(data => this.contacts = data)
            .catch(err => console.log(err))
            
    }
}
</script>

<style scoped> 
.contact_container {
    row-gap: 2.5rem;
}

.contact_content {
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
}

.contact_box {
    background-color: #fff;
    border-radius: .5rem;
    padding: 1.5rem;
    text-align: center;
    box-shadow: 0 4px 6px rgba(174, 190, 205, .3);
}

.contact_icon, .contact_title {
    color: var(--first-color);
}

.contact_icon {
    font-size: 2rem;
}

.contact_title {
    font-size:var(--h3-font-size);
    margin: var(--mb-1) 0;
}

.contact_box:hover {
    box-shadow: 0 6px 8px rgba(174, 190, 205, .4);
}

.contact_inputs {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 1rem;
}

.contact_input, .contact_button {
    outline: none;
    font-family: var(--body-font);
    font-size: var(--normal-font-size);
}

.contact_input {
    width: 100%;
    padding: 1rem;
    border: 2px solid var(--first-color-light);
    color: var(--first-color);
    border-radius: .5rem;
    margin-bottom: var(--mb-1);
}

.contact::placeholder {
    color: var(--first-color-light);
    font-family: var(--body-font);
    font-weight: var(--font-semi-bold);
}

.contact_button {
    cursor: pointer;
    border: none;
}
</style>