<template>
  <div class="testimonial-wrap">
    <div class="main-title text-center">
      <p class="caption-title">
        OUR CUSTOMERS SAID
      </p> <h4>
        They are doing great things with us
      </h4>
    </div>
    <div class="carousel">
      <splide :options="slickOptions">
        <splide-slide
          v-for="(item, index) in testiContent"
          :key="index"
        >
          <div class="item">
            <testi-card
              :text="item.text"
              :avatar="item.avatar"
              :name="item.name"
              class="testi-card"
            />
          </div>
        </splide-slide>
      </splide>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import './testimonials-style';
</style>

<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import imgAPI from '@/assets/images/imgAPI';
import TestiCard from '@/components/Cards/TestiCard';

export default {
  components: {
    Splide,
    SplideSlide,
    TestiCard,
  },
  data() {
    return {
      testiContent: [
        {
          text: 'Sed imperdiet enim ligula, vitae viverra justo porta vel.',
          avatar: imgAPI.avatar[10],
          name: 'Alex Tebalek - CTO La Lieur',
        },
        {
          text: 'Sed imperdiet enim ligula, vitae viverra justo porta vel.',
          avatar: imgAPI.avatar[10],
          name: 'Alex Tebalek - CTO La Lieur',
        },
        {
          text: 'Sed imperdiet enim ligula, vitae viverra justo porta vel.',
          avatar: imgAPI.avatar[10],
          name: 'Alex Tebalek - CTO La Lieur',
        },
        {
          text:
            'Cras convallis lacus orci, tristique tincidunt magna consequat in. In vel pulvinar est, at euismod libero.',
          avatar: imgAPI.avatar[1],
          name: 'Jean Doe - VP Company',
        },
        {
          text:
            'Cras convallis lacus orci, tristique tincidunt magna consequat in. In vel pulvinar est, at euismod libero.',
          avatar: imgAPI.avatar[2],
          name: 'Jena Doe - Graphic Designer',
        },
        {
          text: 'Sed imperdiet enim ligula, vitae viverra justo porta vel.',
          avatar: imgAPI.avatar[3],
          name: 'Jovelin - Senior Graphic Designer',
        },
        {
          text:
            'Cras convallis lacus orci, tristique tincidunt magna consequat in. In vel pulvinar est, at euismod libero.',
          avatar: imgAPI.avatar[4],
          name: 'Jihan Doe - CEO Software House',
        },
        {
          text:
            'Cras convallis lacus orci, tristique tincidunt magna consequat in. In vel pulvinar est, at euismod libero.',
          avatar: imgAPI.avatar[6],
          name: 'Jovelin - Senior Graphic Designer',
        },
        {
          text:
            'Cras convallis lacus orci, tristique tincidunt magna consequat in. In vel pulvinar est, at euismod libero.',
          avatar: imgAPI.avatar[7],
          name: 'Jovelin - Senior Graphic Designer',
        },
      ],
      slickOptions: {
        perPage: 3,
        perMove: 1,
        pagination: false,
        arrows: false,
        type: 'loop',
        breakpoints: {
          360: {
            perPage: 1,
          },
          600: {
            perPage: 2,
          },
          800: {
            perPage: 3,
          },
        },
        reducedMotion: {
          speed: 500,
          rewindSpeed: 1000,
          autoplay: true,
        },
      },
    };
  },
};
</script>
