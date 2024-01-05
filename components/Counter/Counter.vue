<template>
  <div ref="wrapper" v-scroll="runCounter" :class="{ dark: dark }" class="counter-wrap">
    <v-row align="center" justify="center" class="root">
      <v-col>
        <div class="counter-item">
          <!-- <span class="icon ion-ios-leaf-outline" /> -->
          <div class="text">
            <h3 class="text-h3">
              {{ !visible ? 0 : '' }}
              <count-up v-if="visible" :start-val="0" :end-val="2234567" />
            </h3>
            <h6 class="use-text-subtitle2">
              Users and Counting
            </h6>
          </div>
          <div class="action">
            <h4 class="user-text-title2">
              Ready to get started ?
            </h4>
            <v-btn size="large" variant="elevated" color="secondary" class="mx-5 text-white mx-0">
              Get started
            </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<style scoped lang="scss">
@import './counter-style';
</style>

<script>
import CountUp from 'vue-countup-v3';
import { ref } from 'vue';

export default {
  components: {
    CountUp,
  },
  props: {
    dark: {
      type: Boolean,
      default: false,
    },
  },
  setup() {
    const visible = ref(false);
    const wrapper = ref(null);
    const offset = 500;
    function runCounter() {
      const scrollPosition = document.documentElement.scrollTop || document.body.scrollTop;
      const topPosition = scrollPosition + offset;

      if (topPosition > wrapper.value.offsetTop) {
        visible.value = true;
      }
    }

    return {
      visible,
      runCounter,
      wrapper,
    };
  },
  data() {
    return {
      loaded: false,
    };
  },
};
</script>
