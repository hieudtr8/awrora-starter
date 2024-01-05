<template>
  <div class="root-banner">
    <div>
      <div class="inner-deco">
        <div class="cloud-wrap">
          <div class="deco-wrap">
            <div class="cloud-deco" />
          </div>
        </div>
      </div>
    </div>
    <div class="banner-wrap">
      <div class="carousel">
        <splide ref="splide" :options="slickOptions" @splide:active="handleAfterChange">
          <splide-slide>
            <div class="slide mt-5">
              <div class="inner mt-5">
                <v-container class="">
                  <v-row>
                    <v-col cols="12" sm="6" md="6" lg="6">
                      <v-container class="text">
                        <h4 class="use-text-title2">
                          {{ $t('starter.banner_title') }}
                        </h4>
                        <h5 class="use-text-subtitle2">
                          {{ $t('starter.banner_subtitle') }}
                        </h5>
                        <div class="mt-4">
                          <v-btn class="px-0" size="large" color="primary" variant="plain">
                            See detail
                          </v-btn>
                          <v-btn size="large" variant="elevated" color="primary" class="mx-5">
                            Get started
                          </v-btn>
                        </div>
                      </v-container>
                    </v-col>
                    <v-col cols="12" sm="6" md="6" lg="6">
                      <div class="img">
                        <img src="/images/starter/banner1.png" alt="Banner1">
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
          </splide-slide>
          <splide-slide>
            <div class="slide mt-5">
              <div class="inner mt-5">
                <v-container>
                  <v-row>
                    <v-col cols="12" sm="6" md="6" lg="6">
                      <div class="img">
                        <img src="/images/starter/banner2.png" alt="Banner2" class="d-flex justify-end" style="width: 50%; margin: 0px auto; position:relative">
                      </div>
                    </v-col>
                    <v-col cols="12" sm="6" md="6" lg="6">
                      <div class="text">
                        <h4 class="use-text-title2">
                          {{ $t('starter.banner_title') }}
                        </h4>
                        <h5 class="use-text-subtitle2">
                          {{ $t('starter.banner_subtitle') }}
                        </h5>
                        <div class="mt-4">
                          <v-btn class="px-0" size="large" color="primary" variant="plain">
                            See detail
                          </v-btn>
                          <v-btn size="large" variant="elevated" color="primary" class="mx-5">
                            Get started
                          </v-btn>
                        </div>
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
          </splide-slide>
          <splide-slide>
            <div class="slide mt-5">
              <div class="inner mt-5">
                <v-container>
                  <v-row class="justify-end">
                    <v-col cols="12" class="col">
                      <div class="text text-center">
                        <div class="title title-center">
                          <h4 class="use-text-title2">
                            {{ $t('starter.banner_title') }}
                          </h4>
                        </div>
                        <h5 class="use-text-subtitle2">
                          {{ $t('starter.banner_subtitle') }}
                        </h5>
                        <div class="mt-4">
                          <v-btn class="px-0" size="large" color="primary" variant="plain">
                            See detail
                          </v-btn>
                          <v-btn size="large" variant="elevated" color="primary" class="mx-5">
                            Get started
                          </v-btn>
                        </div>
                      </div>
                    </v-col>
                    <v-col cols="12" class="col">
                      <div class="img align-center">
                        <img src="/images/starter/banner3.png" alt="illustration" class="d-flex justify-content-center" style="width: 50%; margin: 0px auto; position:relative">
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
          </splide-slide>
        </splide>
      </div>
      <div class="cloud-top">
        <svg
          width="1273px" height="257px" viewBox="0 0 1273 257" version="1.1"
        >
          <g id="main" transform="translate(0.000000, -10.000000)">
            <g
              id="Cloud-Top"
              transform="translate(628.500000, 205.500000) scale(1, -1) translate(-628.500000, -205.500000) translate(-17.000000, 10.000000)"
            >
              <ellipse id="Oval" cx="235" cy="205" rx="114" ry="95" />
              <ellipse id="Oval" cx="95" cy="161.5" rx="95" ry="78.5" />
              <ellipse id="Oval" cx="429.5" cy="169.5" rx="145.5" ry="121.5" />
              <ellipse id="Oval" cx="678" cy="125.5" rx="151" ry="125.5" />
              <ellipse id="Oval" cx="865.5" cy="174.5" rx="100.5" ry="83.5" />
              <ellipse id="Oval" cx="1095" cy="227.5" rx="196" ry="163.5" />
            </g>
          </g>
        </svg>
      </div>
      <div class="cloud-top-cover">
        <svg
          width="1273px" height="257px" viewBox="0 0 1273 257"
        >
          <g id="main" transform="translate(0.000000, -10.000000)">
            <g
              id="Cloud-Top"
              transform="translate(628.500000, 205.500000) scale(1, -1) translate(-628.500000, -205.500000) translate(-17.000000, 10.000000)"
            >
              <ellipse id="Oval" cx="235" cy="205" rx="114" ry="95" />
              <ellipse id="Oval" cx="95" cy="161.5" rx="95" ry="78.5" />
              <ellipse id="Oval" cx="429.5" cy="169.5" rx="145.5" ry="121.5" />
              <ellipse id="Oval" cx="678" cy="125.5" rx="151" ry="125.5" />
              <ellipse id="Oval" cx="865.5" cy="174.5" rx="100.5" ry="83.5" />
              <ellipse id="Oval" cx="1095" cy="227.5" rx="196" ry="163.5" />
            </g>
          </g>
        </svg>
      </div>
      <hidden point="mdDown">
        <v-container class="max-md">
          <nav class="slide-nav">
            <v-btn
              :class="{ active: currentSlide === 0 }"
              variant="text"
              @click="gotoSlide(0)"
            >
              <strong>First Slide</strong>
              Interdum et malesuada fames ac ante
            </v-btn>
            <v-divider class="divider" vertical inset />
            <v-btn
              :class="{ active: currentSlide === 1 }"
              variant="text"
              @click="gotoSlide(1)"
            >
              <strong>Second Slide</strong>
              Interdum et malesuada fames ac ante
            </v-btn>
            <v-divider class="divider" vertical inset />
            <v-btn
              :class="{ active: currentSlide === 2 }"
              variant="text"
              @click="gotoSlide(2)"
            >
              <strong>Third Slide</strong>
              Interdum et malesuada fames ac ante
            </v-btn>
          </nav>
        </v-container>
      </hidden>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import './slider-styles';
</style>

<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import Hidden from '../Hidden';

export default {
  components: {
    Splide,
    SplideSlide,
    Hidden,
  },
  data() {
    return {
      currentSlide: 0,
      slickOptions: {
        pagination: false,
        arrows: false,
        perPage: 1,
        type: 'loop',
        autoplay: false,
        interval: 100,
        reducedMotion: {
          speed: 1000000,
          rewindSpeed: 10000,
          autoplay: true,
        },
        breakpoints: {
          800: {
            pagination: true,
          },
        },
      },
    };
  },
  methods: {
    handleAfterChange(slide) {
      console.log('🌊 | file: BannerSlider.vue:231 | slide:', slide);
      this.currentSlide = slide.index;
    },
    gotoSlide(index) {
      this.$refs.splide.go(index);
    },
  },
};
</script>
