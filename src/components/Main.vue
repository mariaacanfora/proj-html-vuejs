<template>
      <main>
      <div class="hero-section">
        <div class="container text-center">
          <h4>MOVING WITHOUT THE HASSLE</h4>
          <h1>WE MAKE IT SIMPLE</h1>
          <h4>PROFESSIONAL SERVICE WITH QUALITY AND CUSTOMER SATISFACTION</h4>
        </div>
      </div>

      <div class="free-quote-section">
        <div class="container text-center">
          <h4><i class="fa fa-paper-plane-o" aria-hidden="true"></i> GET A FREE QUOTE ONLINE NOW!</h4>
        </div>
      </div>

      <TxtSection :actualSection="txtSectionList[0]"></TxtSection>
      <!-- <TxtSection class="winning-section" h4Title="HEADACHE FREE" h2Title="Award Winning Moving Company" pTxt="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, amet. Praesentium deserunt debitis repellendus. Blanditiis rerum accusamus aperiam cum est consequuntur magni corporis! Porro blanditiis eos officia dicta quasi quidem." btnTxt="READ OUT TESTIMONIALS"></TxtSection> -->

      <div class="full-service-section general-section">
        <div class="container text-center">
          <h4>WE ARE PROFESSIONAL</h4>
          <h2>Full-Service Solution</h2>
          <div class="row gx-5">        
              <FullServiceCard v-for="(item, i) in fullServiceList" :key="'service' + i" :elementList="item"></FullServiceCard>
          </div>
        </div>
      </div>

      <div class="ease-section general-section">
        <div class="container">
          <div class="row justify-content-end">
              <div class="col-6 text-center">
                <div class="p-3 bg-card">
                  <div class="card-txt">
                    <h4>WE REMOVE THE HEADACHE FROM MOVING</h4>
                    <h2>Move With Ease</h2>
                    <p>With our super simple service we can take you from getting a quote, right through to being in your new home with all of your belongings securely packed and safely delivered, even in the rooms of your choice. </p>
                    <button class="btn rounded-pill personal-btn">GET A FREE QUOTE NOW</button>
                  </div>
                </div>
              </div>
        </div>
        </div>
      </div>

      <div class="testimonial-section general-section">
        <div class="container text-center">
          <h4>HAPPY CUSTOMERS</h4>
          <h2>Testimonials</h2>
          <div class="row">
            <TestimonialCard v-for="(item, i) in testimonialsList" :key="'testimonial' + i" :test="item"></TestimonialCard>
              
          </div>
          <button class="btn rounded-pill personal-btn">READ MORE TESTIMONIALS</button>
        </div>
      </div>

      <TxtSection :actualSection="txtSectionList[1]"></TxtSection>
      <!-- <TxtSection class="request-section" h2Title="Request a Free Quote" pTxt="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, amet. Praesentium deserunt debitis repellendus. Blanditiis rerum accusamus aperiam cum est consequuntur magni corporis! Porro blanditiis eos officia dicta quasi quidem." btnTxt="CLICK HERE"></TxtSection> -->

    </main>
</template>

<script>
import FullServiceCard from './FullServiceCard.vue'
import TestimonialCard from './TestimonialCard.vue'
import TxtSection from './TxtSection.vue'
export default {
  components: { FullServiceCard, TestimonialCard, TxtSection },
name: "Main",
data(){
    return {
        fullServiceList: [
            {
                img: require("../assets/img/avada-movers-serviceonephoto-final-400x255.jpg"),
                title: "Two Man Teams",
                txt: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam voluptatibus corporis, quisquam necessitatibus minus ullam earum quis quo recusandae. Nisi qui consequuntur aliquam ducimus praesentium natus? Alias voluptatum accusantium numquam."
            },

            {
                img: require("../assets/img/avada-movers-servicetwophoto-final-400x255.jpg"),
                title: "We Do All The Lifting",
                txt: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam voluptatibus corporis, quisquam necessitatibus minus ullam earum quis quo recusandae. Nisi qui consequuntur aliquam ducimus praesentium natus? Alias voluptatum accusantium numquam."
            },

            {
                img: require("../assets/img/avada-movers-servicethreephoto-final-400x255.jpg"),
                title: "Coast To Coast",
                txt: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam voluptatibus corporis, quisquam necessitatibus minus ullam earum quis quo recusandae. Nisi qui consequuntur aliquam ducimus praesentium natus? Alias voluptatum accusantium numquam."
            },
        ],

        testimonialsList: [
            {
                img: require("../assets/img/avada-movers-johndoe-final-200x200.jpg"),
                name: "John Doe",
                txt: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita accusamus mollitia aperiam nostrum laborum, beatae perferendis quae excepturi, consequuntur, debitis impedit adipisci delectus omnis magni minus. Quidem voluptatem mollitia molestiae!"
            },

            {
                img: require("../assets/img/avada-movers-janedoe-final-200x200.jpg"),
                name: "Jane Doe",
                txt: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita accusamus mollitia aperiam nostrum laborum, beatae perferendis quae excepturi, consequuntur, debitis impedit adipisci delectus omnis magni minus. Quidem voluptatem mollitia molestiae!"
            },

            {
                img: require("../assets/img/avada-movers-johnsmith-final-200x200.jpg"),
                name: "John Smith",
                txt: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita accusamus mollitia aperiam nostrum laborum, beatae perferendis quae excepturi, consequuntur, debitis impedit adipisci delectus omnis magni minus. Quidem voluptatem mollitia molestiae!"
            },

        ],

        txtSectionList: [
          {
            name: "winning-section",
            h4Title: "HEADACHE FREE",
            h2Title: "Award Winning Moving Company",
            pTxt: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, amet. Praesentium deserunt debitis repellendus. Blanditiis rerum accusamus aperiam cum est consequuntur magni corporis! Porro blanditiis eos officia dicta quasi quidem.",
            btnTxt: "READ OUT TESTIMONIALS"
          },

          {
            name: "request-section",
            h2Title: "Request a Free Quote",
            pTxt: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, amet. Praesentium deserunt debitis repellendus. Blanditiis rerum accusamus aperiam cum est consequuntur magni corporis! Porro blanditiis eos officia dicta quasi quidem.",
            btnTxt: "CLICK HERE"
          },
        ]

    }
}
}
</script>

<style lang="scss">
@import '@/styles/toImport.scss';

main{
  .hero-section{
  background-image: url('../assets/img/avada-movers-homeherobackground-final.jpg');
  background-size: cover;
  background-position: inherit;
  padding-top: $pt-hero;
  padding-bottom: $pb-hero;
}

.free-quote-section{
  padding: $py-base 0;
  background-color: $denim;

  h4{
      color: white;
      font-size: 1rem;
      font-weight: normal;
  }
}

.winning-section{
  background-color: #F2F5F8;
}


.ease-section{
  background-image: url('../assets/img/avada-movers-movewithease-background-new.jpg');
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
  background-image: url('../assets/img/avada-movers-testimonial-background.jpg');
  background-size: cover;
  background-position: top;

  .personal-btn{
    margin-top: 3rem;
  }
}

.request-section{
  background-image: url('../assets/img/avada-movers-request-quote-background.jpg');
  background-size: cover;
  background-position: top;
  border-bottom: 15px solid $lima;
}
}
</style>