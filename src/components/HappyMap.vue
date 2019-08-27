<template>
  <div class="happy-map">
    <div id="allmap"></div>
  </div>
</template>

<script>
export default {
  name: "HappyMap",
  data() {
    return {
      center: { lng: 0, lat: 0 },
      zoom: 3
    };
  },
  mounted() {
    this.initBMap();
  },
  methods: {
    handler() {
      this.center = "深圳市";
      this.zoom = 14;
    },
    initBMap() {
      /*eslint-disable */
      var map = new BMap.Map("allmap"); // 创建地图实例 
      map.centerAndZoom("深圳市", 13); // 初始化地图，设置中心点坐标和地图级别
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.happy-map
  #allmap 
    width: 100vw
    height: 100vh
</style>
