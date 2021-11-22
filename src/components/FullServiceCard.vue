<template>
  <div class="col">
      <div class="p-3 bg-card">
        <img :src="elementList.img" :alt="elementList.title">
        <div class="card-txt">
            <h3>{{elementList.title}}</h3>
            <p>{{elementList.txt}}</p>
            <button class="btn rounded-pill personal-btn">READ MORE</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
name: "FullServiceCard.vue",
props: {
    elementList: Object
}
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';

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
</style>