<template>
  <div class="general-section" :class="actualSection.name">
        <div class="container text-center">
          <h4 v-if="actualSection.h4Title">{{actualSection.h4Title}}</h4>
          <div class="row justify-content-center">
            <div class="col-4"><h2>{{actualSection.h2Title}}</h2></div>
            <div class="col-9"><p>{{actualSection.pTxt}}</p></div>
          </div>
          <button class="btn rounded-pill personal-btn">{{actualSection.btnTxt}}</button>
          
        </div>
    </div>
</template>

<script>
export default {
    name: 'TxtSection',

    props: {
        /* h4Title: String,
        h2Title: String,
        pTxt: String,
        btnTxt: String */
        actualSection: Object
    }
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';

.general-section{
  padding: $py-section 0;
}
</style>