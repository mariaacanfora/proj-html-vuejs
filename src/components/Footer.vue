<template>
  <footer>
      <div class="general-section">
        <div class="container">
          <div class="row">
            <FooterCol :txt="this.txtCol" title="ABOUT"></FooterCol>


            <FooterCol :list="navList" title="AVADA MOVERS"></FooterCol>


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
        linkFooterList: Array,
        infoFooterList: Array,
        iconList: Array
    },

    data(){
        return {
            txtCol: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maiores, enim adipisci. Quasi incidunt similique dolor accusantium labore sequi exercitationem? Eaque voluptatibus quae obcaecati nisi? Aut laudantium earum quo numquam laborum?"
        }
    }
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';

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