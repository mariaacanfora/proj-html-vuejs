<template>
  <header>
      <div class="header-info py-2">
        <div class="container text-light d-flex justify-content-between">
          <span class="fw-normal"> <i class="fa fa-phone" aria-hidden="true"></i> Call us for a Free Wuote: 1.800.55.6789</span>
          <ul class="list-unstyled m-0">
            <li v-for="(icon, i) in iconList" :key="i" class="d-inline-block px-2">
              <a :href="icon.href"><i aria-hidden="true" :class="icon.classIcon" class="text-light"></i></a>
            </li>
          </ul>
        </div>

        <div class="container logo-container py-3 d-flex justify-content-between align-items-center">
          <img src="@/assets/img/avada-movers-logo.png" alt="movers logo">
          <div>
            <ul class="list-unstyled m-0 d-inline-block">
              <li v-for="(item, i) in navList" :key="'A' + i" class="d-inline-block px-4"  @click="onLinkClick(i)" >
                <button class="btn rounded-pill personal-btn" v-if="i === (navList.length - 1)">{{item.link.toUpperCase()}}</button>
                <a v-else href="#" class="text-decoration-none text-dark" :class="{active: i === isActive}">{{item.link}}</a>
              </li>
            </ul>
            
          </div>
        </div>
      </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    props: {
        iconList: Array,
        navList: Array
    },

    data(){
      return {
        isActive: 0
      }
    },

    methods: {
      onLinkClick(it){
        
        this.isActive = it;
        
      }
    }
    
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';


header{
  position: relative;
  
  .header-info{
    background-color: $lima;
  }
  
  .logo-container{
    position: absolute;
    top: 40px;
    left: 0;
    right: 0;

    li, .btn{
      transition: transform .3s;
    }

    li:hover, 
    .btn:hover{
      transform: translateY(-0.2rem);
    }

    .btn:hover{
      color: white;
    }
  }

  .active{
      color: $lima !important;
  }

}
</style>