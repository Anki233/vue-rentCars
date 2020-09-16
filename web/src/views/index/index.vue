<template>
  <div class="amap-wrap">
    <el-amap vid="amapDemo" :zoom="zoom" :center="center" class="amap-demo"></el-amap>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      zoom: 14,
      center: [114.332218,30.521972]
    }
  }
}
</script>

<style lang="scss">
.amap-wrap {
  height: 100vh;
}
</style>