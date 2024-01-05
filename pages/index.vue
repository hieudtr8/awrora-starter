<template>
  <div>
    <div class="main-wrap">
      <main-header home />
      <div class="container-wrap scroll-nav-content">
        <div id="home">
          <banner-slider />
        </div>
        <div id="promotion">
          <promotion />
        </div>
        <div id="feature">
          <v-container>
            <feature />
          </v-container>
        </div>
        <div id="benefit" class="page-section space-bottom-long">
          <benefit />
        </div>
        <div id="integration">
          <integration />
        </div>
        <div id="map" class="space-top">
          <MapMain />
        </div>
        <div id="testimonials" class="space-top">
          <testimonials />
        </div>
        <!-- <div
          id="pricing"
          class="space-top"
        >
          <pricing />
        </div> -->
        <!-- <div id="blog" class="space-top space-bottom">
          <blog />
        </div> -->
        <!-- <div id="subscribe">
          <subscribe />
        </div> -->
      </div>
      <main-footer />
      <hidden point="smDown">
        <corner />
      </hidden>
      <hidden point="mdDown">
        <notification />
      </hidden>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/scss/pages';
</style>

<script>
import { onMounted } from 'vue';
import { useI18n } from 'vue-i18n';
import Header from '@/components/Header';
import Hidden from '@/components/Hidden';
import BannerSlider from '@/components/BannerSlider';
import Promotion from '@/components/Promotion';
import Feature from '@/components/Feature';
import Benefit from '@/components/Benefit';
import Integration from '@/components/Integration';
import MapMain from '@/components/Map';
import Testimonials from '@/components/Testimonials';
import Pricing from '@/components/Pricing';
import Blog from '@/components/Blog';
import Subscribe from '@/components/Subscribe';
import Footer from '@/components/Footer';
import Corner from '@/components/Corner';
import Notification from '@/components/Notification';
import brand from '@/assets/text/brand';
import { defineNuxtComponent, useRouter, useCookie } from '#app';

export default defineNuxtComponent({
  components: {
    'main-header': Header,
    BannerSlider,
    Hidden,
    Promotion,
    Feature,
    Benefit,
    Integration,
    MapMain,
    Testimonials,
    Pricing,
    Blog,
    Subscribe,
    Corner,
    Notification,
    'main-footer': Footer,
  },
  head() {
    return {
      title: brand.starter.name + ' - Home Page',
    };
  },
  setup() {
    // push route to the stored cookie languages only for index page
    const router = useRouter();
    const storedLang = useCookie('i18n_redirected');
    const i18nLocale = useI18n();

    const defaultLocale = '/' + i18nLocale.fallbackLocale.value;
    onMounted(() => {
      const rootUrl = document.location.pathname === '/' || document.location.pathname === defaultLocale;
      if (storedLang.value && rootUrl) {
        router.push({ path: `/${storedLang.value}` });
      }
    });
  },
});
</script>
