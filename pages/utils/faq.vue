<template>
  <div class="main-wrap">
    <main-header />
    <div class="container-wrap">
      <search v-model="keyword" />
      <v-container class="max-md space-top-short">
        <v-row>
          <v-col class="px-6" md="8" cols="12">
            <faq-list />
          </v-col>
          <v-col class="px-6" md="4" cols="12" style="z-index: 10;">
            <div class="space-bottom-short">
              <topic-list />
            </div>
            <div>
              <help-widget />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <main-footer />
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/scss/pages';
</style>

<script>
import brand from '@/assets/text/brand';
import Header from '@/components/Header';
import Footer from '@/components/Footer';
import Search from '@/components/Filter/Search';
import FaqList from '@/components/Faq/FaqList';
import TopicList from '@/components/Faq/TopicList';
import HelpWidget from '@/components/List/Sidebar/HelpWidget';

export default {
  components: {
    'main-header': Header,
    'main-footer': Footer,
    Search,
    FaqList,
    TopicList,
    HelpWidget,
  },
  data() {
    return {
      keyword: '',
    };
  },
  head() {
    return {
      title: brand.starter.name + ' - Faq',
    };
  },
};
</script>
