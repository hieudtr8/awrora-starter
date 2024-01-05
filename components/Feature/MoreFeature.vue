<template>
  <div class="feature-more">
    <v-container>
      <v-row id="feature1" class="feature-item">
        <v-col md="6" class="px-6" cols="12">
          <div data-aos="zoom-in" data-aos-delay="300" data-aos-duration="600">
            <!-- <div class="deco1" /> -->
          </div>
          <div data-aos="fade-right" data-aos-delay="500" data-aos-duration="600">
            <figure class="img">
              <img src="/images/starter/feature1.png" alt="img">
            </figure>
          </div>
        </v-col>
        <v-col md="6" class="px-6" cols="12">
          <div data-aos="fade-left" data-aos-duration="600">
            <p class="caption-title text-center text-md-start">
              EASY INTEGRATIONS
            </p>
            <h3 class="text-center text-md-start use-text-title mb-6">
              Fast, Secure And Always Online.
            </h3>
          </div>
          <div data-aos="fade-left" data-aos-delay="300" data-aos-duration="600">
            <p class="text-center text-md-start use-text-caption pb-1">
              With industry-leading load times, guaranteed 99.9% uptime and expert, 24/7 support, your site couldn’t ask
              for more.
            </p>
            <v-btn size="small" variant="elevated" color="primary" class="mt-5 button-learn-more left">
              Learn More
            </v-btn>
          </div>
        </v-col>
      </v-row>
      <hr aria-orientation="horizontal" class="divider v-divider">
      <v-row id="feature2" class="feature-item">
        <v-col md="6" class="px-6" cols="12">
          <div data-aos="fade-left" data-aos-duration="600">
            <p class="caption-title text-center text-md-end">
              SMART DEPLOYMENT
            </p>
            <h3 class="text-center text-md-end use-text-title mb-6 display-2">
              Deploy And Scale Seamlessly
            </h3>
          </div>
          <div data-aos="fade-right" data-aos-delay="500" data-aos-duration="600">
            <p class="text-center text-md-end use-text-caption">
              Deploy to any of our data center locations – New York, SF, London, Amsterdam, Bangalore, and more.
            </p>
            <v-btn size="small" variant="elevated" color="primary" class="mt-5 button-learn-more right">
              Learn More
            </v-btn>
          </div>
        </v-col>
        <v-col md="6" class="px-6 mt-md-5" cols="12">
          <div data-aos="zoom-in" data-aos-delay="300" data-aos-duration="600">
            <!-- <div class="deco1" /> -->
          </div>
          <div data-aos="fade-left" data-aos-delay="500" data-aos-duration="600">
            <figure class="img">
              <img src="/images/starter/feature2.png" alt="img">
            </figure>
          </div>
        </v-col>
        <!-- :order="isTablet ? 'last' : 'first'" -->
      </v-row>
      <!-- <v-row>
        <v-col md="12" class="px-6" cols="12">
          <div class="last text-center">
            <div data-aos="fade-up" data-aos-duration="600">
              <h3 class="use-text-title mb-6 display-2">
                Lorem ipsum dolor
              </h3>
            </div>
            <div data-aos="fade-up" duration="0.6s" delay="0.3s">
              <p class="text">
                Quos blanditiis tenetur unde suscipit,
                quam beatae rerum inventore consectetur,
                neque doloribus.
              </p>
            </div>
            <div data-aos="zoom-in" data-aos-duration="600" data-aos-delay="300">
              <div class="deco2" />
            </div>
            <div data-aos="fade-up" data-aos-duration="600" data-aos-delay="500">
              <figure class="img-full">
                <img :src="imgAPI.photo[1]" alt="img">
              </figure>
            </div>
          </div>
        </v-col>
      </v-row> -->
    </v-container>
  </div>
</template>

<style scoped lang="scss">
@import './feature-styles';
</style>

<script>
import AOS from 'aos';
import imgAPI from '@/assets/images/imgAPI';

export default {
  data() {
    return {
      imgAPI,
    };
  },
  computed: {
    isTablet() {
      const mdDown = this.$vuetify.display.smAndDown;
      return mdDown;
    },
  },
  mounted() {
    AOS.init({
      once: true,
    });
  },
};
</script>
