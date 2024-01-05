<template>
  <div class="hero-banner-wrap">
    <div class="inner">
      <div class="inner-deco">
        <div class="deco-wrap">
          <div class="cloud-deco" />
        </div>
      </div>
      <v-container style="z-index: 1;">
        <v-row align="center" justify="center">
          <v-col lg="7" sm="6" class="px-5">
            <div class="text text-center text-sm-start">
              <h4 class="text-h4">
                Pellentesque habitant morbi tristique senectus
              </h4>
              <h5 class="text-h5">
                Multiple lines of text that form the lede, informing new readers quickly and efficiently about what's most interesting in this post's contents
              </h5>
            </div>
          </v-col>
          <v-col lg="3" sm="6" class="px-5">
            <div class="img">
              <img src="/images/starter/about1.png" alt="illustration">
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import './about-style.scss';
</style>
