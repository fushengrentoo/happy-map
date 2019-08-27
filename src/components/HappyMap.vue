<template>
  <div class="happy-map">
    <baidu-map
      :center="center"
      :zoom="zoom"
      @ready="handler"
      class="map"
      ak="D74e2300cc18a93aa99b8715eeb122e5"
    ></baidu-map>
  </div>
</template>

<script>
import BaiduMap from "vue-baidu-map/components/map/Map.vue";

export default {
  name: "HappyMap",
  components: {
    BaiduMap
  },
  props: {},
  data() {
    return {
      center: { lng: 0, lat: 0 },
      zoom: 3
    };
  },
  methods: {
    handler() {
      this.center.lng = 116.404;
      this.center.lat = 39.915;
      this.zoom = 15;
    }    
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.happy-map
  .map 
    width: 100vw
    height: 100vh
</style>
