<template>
  <div class="footer-counter extend">
    <div class="round" />
    <div id="counter" class="page-section">
      <counter />
    </div>
    <basic v-if="type === 'basic'" />
    <blog v-if="type === 'blog'" />
    <contact-footer v-if="type === 'contact'" />
    <site-map v-if="type === 'sitemap'" />
    <div class="building-deco">
      <img src="/images/starter/footer1.png" alt="">
      <img src="/images/starter/footer2.png" alt="">
      <img src="/images/starter/footer1.png" alt="">
    </div>
  </div>
</template>
<style scoped lang="scss">
@import './footer-main';
</style>
<script>
import ui from '@/composables/uiTheme';
import Basic from './Basic';
import Blog from './Blog';
import Contact from './Contact';
import SiteMap from './SiteMap';
import Counter from '@/components/Counter';

export default {
  components: {
    Basic,
    Blog,
    'contact-footer': Contact,
    SiteMap,
    Counter,
  },
  setup() {
    const type = ui.footer();
    return {
      type,
    };
  },
};
</script>
