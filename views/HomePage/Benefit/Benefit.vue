<template>
  <div
    class="benefit-wrap"
  >
    <section id="benefit">
      <div class="root">
        <div class="illustration-bg">
          <img :src="`/images/starter/benefit_bg.png`" alt="Benefit background" class="img-2d3d">
        </div>
        <v-container class="container max-md">
          <div class="wrapper">
            <div class="desc">
              <div class="main-title center dark">
                <p class="caption-title">
                  benefit
                </p>
                <h4>
                  Trust your cloud
                </h4>
              </div>
              <p class="use-text-subtitle2">
                Web hosting made easy &amp; affordable! FREE Get Your Domain On! 1 Year Domain Registration on Shared Annual Plans
              </p>
              <div class="carousel">
                <splide ref="splide" :options="slickOptions" @splide:active="handleAfterChange">
                  <splide-slide v-for="index in 4" :key="index" class=" d-flex justify-center align-center">
                    <div class="slide">
                      <div class="inner">
                        <v-container>
                          <div class="justify-center">
                            <div class="border-image">
                              <figure>
                                <img :src="`/images/starter/benefit${index}.jpg`" :alt="`Banner${index}`">
                              </figure>
                            </div>
                          </div>
                        </v-container>
                      </div>
                    </div>
                  </splide-slide>
                </splide>
              </div>
            </div>
          </div>
        </v-container>
      </div>
    </section>
  </div>
</template>

<style scoped lang="scss">
@import './benefit-style';
</style>

<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';

export default {
  components: {
    Splide,
    SplideSlide,
  },
  data() {
    return {
      currentSlide: 0,
      slickOptions: {
        arrows: true,
        pagination: true,
        perPage: 1,
        type: 'fade',
        rewind: true,
        autoplay: false,
        interval: 1000,
        reducedMotion: {
          speed: 1000,
          rewindSpeed: 1000,
          autoplay: true,
        },
      },
    };
  },
  methods: {
    handleAfterChange(slide) {
      this.currentSlide = slide.index;
    },
    gotoSlide(index) {
      this.$refs.splide.go(index);
    },
  },
};
</script>
