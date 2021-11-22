<template>
  <div id="app">
    <header>
      <div class="header-info py-2">
        <div class="container text-light d-flex justify-content-between">
          <span> <i class="fa fa-phone" aria-hidden="true"></i> Call us for a Free Wuote: 1.800.55.6789</span>
          <ul class="list-unstyled m-0">
            <li v-for="(icon, i) in iconHeaderList" :key="i" class="d-inline-block px-2">
              <a :href="icon.href"><i aria-hidden="true" :class="icon.classIcon" class="text-light"></i></a>
            </li>
          </ul>
        </div>

        <div class="container logo-container py-3 d-flex justify-content-between align-items-center">
          <img src="@/assets/img/avada-movers-logo.png" alt="">
          <div>
            <ul class="list-unstyled m-0 d-inline-block">
              <li v-for="(item, i) in linkHeaderList" :key="i" class="d-inline-block px-4">
                <a :href="item.href" class="text-decoration-none text-dark">{{item.link}}</a>
              </li>
            </ul>
            <button class="btn rounded-pill btn-color">FREE QUOTE</button>
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    
  },

  data(){
    return{
      iconHeaderList: [
        {
          classIcon: "fa fa-facebook",
          href: '/facebook'
        },

        {
          classIcon: "fa fa-twitter",
          href: '/twitter'
        },

        {
          classIcon: "fa fa-instagram",
          href: '/instagram'
        },

        {
          classIcon: "fa fa-youtube-play",
          href: '/youtube'
        },
      ],

      linkHeaderList: [
        {
          link: "Home",
          href: "/home"
        },

        {
          link: "Rates",
          href: "/rates"
        },

        {
          link: "Testimonials",
          href: "/testimonials"
        },

        {
          link: "FAQ",
          href: "/faq"
        },

        {
          link: "Blog",
          href: "/blog"
        },

        {
          link: "Contact",
          href: "/contact"
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';
@import '@/styles/variables.scss';
@import '~font-awesome/css/font-awesome.css';

header{
  position: relative;
}

.header-info{
  background-color: $lima;
}

.logo-container{
  position: absolute;
  top: 40px;
  left: 0;
  right: 0;
}

.btn-color{
  background-color: $denim;
  color: white;
  padding: 0.375rem 1.25rem;
}

/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
