<template>
  <section class="portfolio section bd-container" id="portfolio">
            <span class="section-subtitle">My recent works</span>
            <h2 class="section-title">Portfolio</h2>

            <div class="portfolio_nav">
                <span class="portfolio_item active-portfolio" data-filter="all">All</span>
                <span class="portfolio_item" data-filter=".web">Web</span>
                <span class="portfolio_item" data-filter=".ux">UI/UX</span>
            </div>

            <div class="portfolio_container bd-grid"  id="portfolio-content" :key="port" v-for="port in portfolio">
                 <div class="portfolio_content mix {{port.class}}">
                    <a href="#"><img src="{{port.img}}" alt="" class="portfolio_img"></a>
                      <div class="portfolio_data">
                          <span class="portfolio_subtitle">{{port.name}}</span>
                          <a href="#"><h2 class="portfolio_title">{{port.title}}</h2></a>
                          <a href="#" class="button button-link">{{port.link}}</a>
                      </div>
                </div>
            </div>
        </section>
</template>

<script>
export default {

    data(){
        return{
            portfolio:[]
        }
    },
 mounted() {
     
        fetch('http://localhost:3000/portfolio')
            .then(res => res.json())
            .then(data => this.portfolio = data)
            .catch(err => console.log(err))
            
    }
}
</script>

<style scoped>
.portfolio_nav {
    text-align: center;
    margin-bottom: var(--mb-3);
    font-weight: lighter;
}

.portfolio_item {
    margin: 0 var(--mb-2);
    cursor: pointer;
}

.portfolio_content {
    background-color: #fff;
    border-radius: .5rem;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(174, 190, 205, .3);
}

.portfolio_img {
    width: 100%;
    transition: .4s;
}

.portfolio_data {
    padding: 1.5rem;
}

.portfolio_subtitle {
    font-size: var(--small-font-size);
    color: var(--first-color-light);
}

.portfolio_title {
    font-size: var(--h3-font-size);
    color: var(--first-color);
    margin: var(--mb-2) 0;
}

.portfolio_content:hover {
    box-shadow: rgba(174, 190, 205, .4) ;
}

.portfolio_content:hover, .portfolio_img{
    transform: scale(1.02);
}

/* Active menu portfolio */
.active-portfolio {
    color: var(--first-color-dark);
    font-weight: var(--font-bold);
}
</style>