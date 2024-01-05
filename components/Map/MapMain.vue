<template>
  <div class="map-wrap">
    <section id="map-container">
      <div class="root">
        <v-container class="container">
          <div class="main-title center">
            <p class="caption-title">
              All you need to grow online.
            </p>
            <h4>
              Deploy and scale seamlessly
            </h4>
          </div>
          <v-row>
            <v-col md="7" cols="12" class="map-wrap">
              <div class="world-map">
                <div class="location-wrap">
                  <div v-for="(location,i) in locations" :key="i" class="location-item" :style="{ 'left': location[0] + 'px', 'top': location[1] + 'px' }">
                    <v-btn variant="elevated" :class="{ 'primary': i % 2 == 0, 'secondary': i % 2 !== 0 }">
                      <v-tooltip
                        activator="parent"
                        location="top"
                      >
                        {{ `Location: ` + i }}
                      </v-tooltip>
                      <v-icon>mdi-square-rounded</v-icon>
                    </v-btn>
                  </div>
                </div>
              </div>
            </v-col>
            <v-col md="5" cols="12">
              <div class="text">
                <section>
                  <div class="" style="">
                    <div class="px-4">
                      <h3 class="use-text-subtitle title-primary">
                        <span />
                        Region A
                      </h3>
                      <p class="use-text-paragraph">
                        Aliquam nec ex aliquet, aliquam neque non, gravida est. Vestibulum nec mi suscipit, dapibus purus
                        a, imperdiet tellus.
                      </p>
                    </div>
                  </div>
                  <div class="" style="">
                    <div class="px-4">
                      <h3 class="use-text-subtitle title-secondary">
                        <span />
                        Region B
                      </h3>
                      <p class="use-text-paragraph">
                        Aliquam nec ex aliquet, aliquam neque non, gravida est. Vestibulum nec mi suscipit, dapibus purus
                        a, imperdiet tellus.
                      </p>
                    </div>
                  </div>
                </section>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </section>
  </div>
</template>

<style scoped lang="scss">
@import './map-style';
</style>

<script>

export default {
  data() {
    return {
      locations:
        [
          [100, 150],
          [120, 100],
          [400, 40],
          [500, 300],
          [270, 200],
          [10, 40],
          [330, 100],
          [30, 50],
          [480, 100],
          [250, 100],
          [120, 300],
          [300, 140],
          [480, 280],
          [300, 100],
        ],
    };
  },
  created() {
    console.log(this.locations);
  },
};
</script>
