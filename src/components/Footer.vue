<template>
  <footer>
      <div class="general-section">
        <div class="container">
          <div class="row">
            <FooterCol :txt="txtCol" title="ABOUT"></FooterCol>


            <FooterCol :list="footerList" title="AVADA MOVERS" v-model="activeIndex"></FooterCol>

          
            <FooterCol :list="linkFooterList" title="RECENT POST"></FooterCol>
          </div>
        </div>
      </div>

      <div class="footer-info-section">
        <div class="container text-center">
          <ul class="list-unstyled list-info">
            <li v-for="(item, i) in infoFooterList" :key="'D'+ i" class="d-inline-block"> <i :class="item.iconClass" aria-hidden="true"></i> <a :href="item.href">{{item.link}}</a> <span v-if="item !== infoFooterList[infoFooterList.length - 1]"> |</span></li>
          </ul>

          <ul class="list-unstyled m-0">
            <li v-for="(icon, i) in iconList" :key="'E' + i" class="d-inline-block px-2">
              <a :href="icon.href"><i aria-hidden="true" :class="icon.classIcon" class="text-light"></i></a>
            </li>
          </ul>
        </div>
      </div>
      
    </footer>
</template>

<script>
import FooterCol from './FooterCol.vue'
export default {
  components: { FooterCol },
  name: "Footer",
  props: {
      navList: Array,
      iconList: Array
  },

  data(){
      return {
          txtCol: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maiores, enim adipisci. Quasi incidunt similique dolor accusantium labore sequi exercitationem? Eaque voluptatibus quae obcaecati nisi? Aut laudantium earum quo numquam laborum?",
          
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
          ],

          activeIndex: 0
      }
  },

  computed: {
    footerList(){
    let newList = this.navList.filter((element) => {
      return (element.link != "FAQ" && element.link != "Contact")
    })
    console.log(newList);
    return newList
  }
  },
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';

footer{
  .row{
      li:hover{
        transform: translateX(0.2rem);   
      }
  }

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