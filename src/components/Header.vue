<template>
  <header>
      <div class="header-info py-2">
        <div class="container text-light d-flex justify-content-between">
          <span> <i class="fa fa-phone" aria-hidden="true"></i> Call us for a Free Wuote: 1.800.55.6789</span>
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
              <li v-for="(item, i) in navList" :key="'A' + i" class="d-inline-block px-4">
                <a :href="item.href" class="text-decoration-none text-dark">{{item.link}}</a>
              </li>
            </ul>
            <button class="btn rounded-pill personal-btn">FREE QUOTE</button>
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
  }
}
</style>