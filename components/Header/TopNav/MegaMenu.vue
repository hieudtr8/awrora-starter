<template>
  <div class="multi-menu">
    <template
      v-for="(item, index) in dataMenu"
      :key="index"
    >
      <!-- Multilevel Nav -->
      <v-menu
        v-if="item.child"
        :open-on-hover="hover"
        :position-x="0"
        max-height="480"
        offset-y
        content-class="mega-menu-root"
        width="100%"
        transition="slide-y-transition"
        nudge-left
        nudge-width
      >
        <template #activator="{ props }">
          <span
            class="button-item"
            v-bind="props"
          >
            <v-btn text>
              {{ item.name }}
              <v-icon right>
                mdi-chevron-down
              </v-icon>
            </v-btn>
          </span>
        </template>
        <div class="mega-menu">
          <v-container class="max-md">
            <v-row>
              <v-col
                v-for="(subitem, index) in item.child"
                :key="index"
                sm="3"
              >
                <v-list>
                  <v-list-subheader class="title-mega">
                    {{ subitem.name }}
                  </v-list-subheader>
                  <img :src="subitem.thumb" alt="thumbnail" class="thumb-menu">
                  <div>
                    <v-list-item
                      v-for="(item, index) in subitem.child"
                      :key="index"
                      :href="item.link"
                      :class="{ current: curURL === (curOrigin+langPath+item.link)}"
                    >
                      <div>
                        <v-list-item-title class="menu-list" v-text="item.name" />
                      </div>
                    </v-list-item>
                  </div>
                </v-list>
              </v-col>
            </v-row>
          </v-container>
        </div>
      </v-menu>
      <!-- Single Nav -->
      <v-btn
        v-else
        v-smooth-scroll="{ offset: -100 }"
        :href="item.link"
        :class="{ current: curURL === (curOrigin+langPath+item.link)}"
        text
        @click="handleNavigate(item.link)"
      >
        {{ item.name }}
      </v-btn>
    </template>
  </div>
</template>

<style lang="scss" scoped>
@import '../header-style.scss';
</style>

<script>
import navMenu from '../data/single';

let counter = 0;
function createData(name, link, offset) {
  counter += 1;
  return {
    id: counter,
    name,
    link,
    offset,
  };
}

export default {
  props: {
    home: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      fixed: false,
      sections: {},
      activeMenu: '',
      openNavMobile: null,
      dataMenu: [
        createData(navMenu[0], '#' + navMenu[0]),
        createData(navMenu[1], '#' + navMenu[1]),
        createData(navMenu[2], '#' + navMenu[2]),
        createData(navMenu[3], '#' + navMenu[3], -40),
        createData(navMenu[4], '#' + navMenu[4], -40),
      ],
    };
  },
  computed: {
    isTablet() {
      const mdDown = this.$vuetify.display.mdAndDown;
      return mdDown;
    },
    isDesktop() {
      const lgUp = this.$vuetify.display.lgAndUp;
      return lgUp;
    },
  },
  mounted() {
    const section = document.querySelectorAll('.scroll-nav-content > *');
    console.log('🌊 | file: MegaMenu.vue:131 | section:', section);
    Array.prototype.forEach.call(section, (e) => {
      this.sections[e.id] = e.offsetTop;
    });
  },
  methods: {
    handleScroll() {
      const scrollPosition = document.documentElement.scrollTop || document.body.scrollTop;
      const topPosition = scrollPosition + 100;

      Object.keys(this.sections).forEach((i) => {
        if (this.sections[i] <= topPosition) {
          this.activeMenu = i;
        }
      });

      if (scrollPosition > 70) {
        this.fixed = true;
      } else {
        this.fixed = false;
      }
    },
    handleToggleOpen() {
      this.openNavMobile = !this.openNavMobile;
    },
  },
};
</script>
