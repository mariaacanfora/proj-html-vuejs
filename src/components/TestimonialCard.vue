<template>
  <div class="col">
    <div class="testimonial-container">
      <img :src="test.img" :alt="test.name" class="rounded-circle w-25"/>
      <h3>{{test.name}}</h3>
      <p>"{{test.txt}}"</p>
    </div>
  </div>
</template>

<script>
export default {
    name: "TestimonialCard",
    props: {
        test: Object
    }
};
</script>

<style lang="scss">
.testimonial-container{
  p{
    font-style: italic;
  }
}
</style>