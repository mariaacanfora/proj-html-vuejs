<template>
  <div id="app">
    <Header :navList="navList" :iconList="iconList"></Header>

    <Main></Main>

    <Footer :iconList="iconList" :navList="navList"></Footer>

  </div>
</template>

<script>
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },

  data(){
    return{
      iconList: [
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

      navList: [
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

        {
          link: "Free Quote",
          href: "/free quote"
        }
      ],
    }
  },
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';

body{
  
  font-weight: bold;

  h1{
    font-size: 3rem;
    font-weight: bold;
  }

  h2{
    font-size: 2.5rem;
    font-weight: bold;
    padding-bottom: 2rem;
    color: $lima;
  }

  h3{
    font-size: 2rem;
    font-weight: bold;
    color: $denim;
    padding: 1rem;
  }

  h4{
    font-size: 1rem;
    font-weight: bold;
    padding-bottom: 0.75rem;
    color: $silver-chalince;
  }

  p{
    font-weight: normal;
    padding-bottom: 2rem;
  }

  .btn{
    transition: transform .3s;
  }

  .btn:hover{
      transform: scale(1.1);
      color: white;
  }

  .personal-btn{
    background-color: $denim;
    color: white;
    padding: 0.375rem 1.25rem;
    font-weight: bold;
  }
}
</style>
