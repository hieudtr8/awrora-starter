<template>
  <div class="page-section main-promotion">
    <div class="banner-wrap">
      <div class="carousel ">
        <splide ref="splide" :options="slickOptions" @splide:active="handleAfterChange">
          <splide-slide class=" d-flex justify-center align-center">
            <div class="slide">
              <div class="inner">
                <v-container>
                  <v-row class="justify-center">
                    <v-col cols="12" sm="6" md="5" lg="5">
                      <section class="image-icon d-flex justify-center align-center">
                        <v-icon>
                          mdi-cube-outline
                        </v-icon>
                      </section>
                    </v-col>
                    <v-col class="text-container" cols="12" sm="6" md="7" lg="7">
                      <div class="text">
                        <h1 class="use-text-title2">
                          <v-btn color="secondary" variant="text" class="px-0">
                            Wordpress Hosting start from $2/mo
                          </v-btn>
                        </h1>
                        <h6 class="use-text-subtitle2">
                          Sed imh6erdiet enim ligula vitae viverra. Vivamus sit amet interdum elit.
                        </h6>
                        <section class="time">
                          <h6 class="use-text-caption">
                            <span>
                              periode
                              :&nbsp;
                              12 Jul - 10 Aug
                            </span>
                          </h6>
                        </section>
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
          </splide-slide>
          <splide-slide class=" d-flex justify-center align-center">
            <div class="slide">
              <div class="inner">
                <v-container>
                  <v-row class="justify-center">
                    <v-col cols="12" sm="6" md="5" lg="5">
                      <section class="image-icon d-flex flex-column  justify-center align-center">
                        <v-icon>
                          mdi-toggle-switch-off-outline
                        </v-icon>
                        <v-icon>
                          mdi-toggle-switch-outline
                        </v-icon>
                      </section>
                    </v-col>
                    <v-col class="text-container" cols="12" sm="6" md="7" lg="7">
                      <div class="text">
                        <h1 class="use-text-title2">
                          <v-btn color="secondary" variant="text" class="px-0">
                            Wordpress Hosting start from $2/mo
                          </v-btn>
                        </h1>
                        <h6 class="use-text-subtitle2">
                          Sed imh6erdiet enim ligula vitae viverra. Vivamus sit amet interdum elit.
                        </h6>
                        <section class="time">
                          <h6 class="use-text-caption">
                            <span>
                              periode
                              :&nbsp;
                              12 Jul - 10 Aug
                            </span>
                          </h6>
                        </section>
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
          </splide-slide>
          <splide-slide class=" d-flex justify-center align-center">
            <div class="slide">
              <div class="inner">
                <v-container>
                  <v-row class="justify-center">
                    <v-col cols="12" sm="6" md="5" lg="5">
                      <section class="image-icon d-flex justify-center align-center">
                        <v-icon>
                          mdi-folder-star-multiple-outline
                        </v-icon>
                      </section>
                    </v-col>
                    <v-col class="text-container" cols="12" sm="6" md="7" lg="7">
                      <div class="text">
                        <h1 class="use-text-title2">
                          <v-btn color="secondary" variant="text" class="px-0">
                            Wordpress Hosting start from $2/mo
                          </v-btn>
                        </h1>
                        <h6 class="use-text-subtitle2">
                          Sed imh6erdiet enim ligula vitae viverra. Vivamus sit amet interdum elit.
                        </h6>
                        <section class="time">
                          <h6 class="use-text-caption">
                            <span>
                              periode
                              :&nbsp;
                              12 Jul - 10 Aug
                            </span>
                          </h6>
                        </section>
                      </div>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
          </splide-slide>
        </splide>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import './promotion-styles';
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
        pagination: false,
        perPage: 1,
        type: 'loop',
        autoplay: false,
        interval: 1000,
        reducedMotion: {
          speed: 1000,
          rewindSpeed: 1000,
          autoplay: true,
        },
      },
      svg: '',
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
