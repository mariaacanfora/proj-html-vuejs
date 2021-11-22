<template>
  <div id="app">
    <Header :navList="navList" :iconList="iconList"></Header>

    <Main></Main>


    <footer>
      <div class="general-section">
        <div class="container">
          <div class="row">
            <div class="col-4">
              <h4>
                ABOUT
              </h4>
              <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maiores, enim adipisci. Quasi incidunt similique dolor accusantium labore sequi exercitationem? Eaque voluptatibus quae obcaecati nisi? Aut laudantium earum quo numquam laborum?</p>
              <img src="@/assets/img/avada-movers-logo.png" alt="movers logo">
            </div>

            <div class="col-4">
              <h4>
                AVADA MOVERS
              </h4>
              <ul class="list-unstyled">
                <li v-for="(item, i) in linkHeaderList" :key="'B' + i" class="py-3">
                  > <a :href="item.href" class="text-dark">{{item.link}}</a>
                </li>
              </ul>
            </div>

            <div class="col-4">
              <h4>
                RECENT POSTS
              </h4>
              <ul class="list-unstyled">
                <li v-for="(item, i) in linkFooterList" :key="'C' + i" class="py-3">
                  > <a :href="item.href" class="text-dark">{{item.link}}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <div class="footer-info-section">
        <div class="container text-center">
          <ul class="list-unstyled list-info">
            <li v-for="(item, i) in infoFooterList" :key="'D'+ i" class="d-inline-block"> <i :class="item.iconClass" aria-hidden="true"></i> <a :href="item.href">{{item.link}}</a> <span v-if="item !== infoFooterList[infoFooterList.length - 1]"> |</span></li>
          </ul>

          <ul class="list-unstyled m-0">
            <li v-for="(icon, i) in iconHeaderList" :key="'E' + i" class="d-inline-block px-2">
              <a :href="icon.href"><i aria-hidden="true" :class="icon.classIcon" class="text-light"></i></a>
            </li>
          </ul>
        </div>
      </div>
      
    </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main
    
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
      ],

      linkFooterList:[
        {
          link: "Heading Out To College?",
          href:"/heading-out-to-college"
        },

        {
          link: "Moving Your Business?",
          href:"/moving-your-business"
        },

        {
          link: "Outstanding Quality",
          href:"/outstanding-quality"
        },

        {
          link: "Cost of Moving",
          href:"/cost-of-moving"
        },
        
        {
          link: "Best Moving Tips",
          href:"/best-moving-tips"
        },
        
      ],

      infoFooterList: [
        {
          link: "Copyright 2012 - 2020",
          href: "/copyright",
          iconClass: "fa fa-copyright"
        },

        {
          link: "Avada Theme by ThemeFusion",
          href: "/avada",
          iconClass: "d-none"
        },

        {
          link: "All Rights Reserved",
          href: "/rights-reserved",
          iconClass: "d-none"
        },

        {
          link: "Powered by WordPress",
          href: "/wordpress",
          iconClass: "d-none"
        },
      ]
    }
  }
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
    font-size: 0.85rem;
    font-weight: bold;
    padding-bottom: 0.75rem;
    color: $silver-chalince;
  }

  p{
    font-weight: normal;
    padding-bottom: 2rem;
  }

  .personal-btn{
    background-color: $denim;
    color: white;
    padding: 0.375rem 1.25rem;
    font-weight: bold;
  }
}

//MAIN

main{
  .hero-section{
  background-image: url('./assets/img/avada-movers-homeherobackground-final.jpg');
  background-size: 110%;
  background-position: inherit;
  padding-top: $pt-hero;
  padding-bottom: $pb-hero;
}

.free-quote-section{
  padding: $py-base 0;
  background-color: $denim;
}

.general-section{
  padding: $py-section 0;
}

.winning-section{
  background-color: $mercury;
}

.full-service-section{
  
  img{
    width: 100%;
    margin-bottom: 1rem;
  }


  .bg-card{
    background-color: #F2F5F8;
  }
  .card-txt{
    background-color: white;

    p{
      padding: 0 0.5rem
    }

    .personal-btn{
      margin: 2rem 0;
    }
    
  }
}

.ease-section{
  background-image: url('./assets/img/avada-movers-movewithease-background-new.jpg');
  background-size: cover;
  background-position: top;

  .bg-card{
    background-color: $mantis;
    border: 15px solid #5AA511;
  }

  .card-txt{
    h2, h4{
    color: white;
    }
    color: white;
    padding: 2rem;
  }
}

.testimonial-section{
  background-image: url('./assets/img/avada-movers-testimonial-background.jpg');
  background-size: cover;
  background-position: top;

  .personal-btn{
    margin-top: 3rem;
  }
}

.request-section{
  background-image: url('./assets/img/avada-movers-request-quote-background.jpg');
  background-size: cover;
  background-position: top;
  border-bottom: 15px solid $lima;
}
}

//FOOTER
footer{
  a{
    text-decoration: none;    
    font-weight: normal;
    font-size: 1.25rem;
  }

  .general-section{
    padding: $py-base 0;
  }

  .footer-info-section{
    background-color: $lima;
    padding: $py-base 0;
    color: white;
    font-weight: normal;

    .list-info{
      a{
        color: white;
        font-size: 0.85rem;
        padding: 0 0.25rem;
      }

    }

  }
}

</style>
