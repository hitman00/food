<template>
  <div :class="$style.main">
    <HeaderMain />
    <div :class="$style.max_size">
      <Bike />
      <Slider />
    </div>
    <GetStart />
    <Footer />
  </div>
</template>

<script>
import HeaderMain from '@/components/HeaderMain/HederMain.vue'
import Bike from '@/components/Bike/Bike.vue'
import Slider from '@/components/Slider/Slider.vue'
import GetStart from '@/components/GetStart/GetStart.vue'
import Footer from '@/components/Footer/Footer.vue'
export default {
  components: {
    HeaderMain,
    Bike,
    Slider,
    GetStart,
    Footer,
  },
}
</script>

<style lang="scss" module>
.main {
  margin: 0 auto;
}

.max_size {
  max-width: 1200px;
  padding-left: 15px;
  padding-right: 15px;
  margin: 0 auto;
}
</style>
