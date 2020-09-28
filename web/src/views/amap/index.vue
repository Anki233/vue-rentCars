<template>
  <div class="amap-wrap">
    <el-amap vid="amapContainer" :events="events"
             class="amap-demo"></el-amap>
  </div>
</template>

<script>
import {AMapManager, lazyAMapApiLoaderInstance} from 'vue-amap';

export default {
  name: "Amap",
  data() {
    return {
      map: null,
      zoom:15,
      events: {}
    }
  },
  mounted() {
    lazyAMapApiLoaderInstance.load().then(() => {
      // your code ...
      this.map = new AMap.Map('amapContainer', {
        zoom: this.zoom,
        center: [114.333427, 30.372905]
      });
    });
  }
}
</script>

<style lang="scss">
.amap-wrap {
  height: 100vh;
}
</style>