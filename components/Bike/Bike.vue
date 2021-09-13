<template>
  <div :class="$style.men_main">
    <div :class="$style.men_image">
      <img src="@/assets/imgs/22.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Bike',
}
</script>

<style lang="scss" module>
.men_main {
  display: flex;
  justify-content: end;
}

.men_image {
  position: relative;
  width: 35%;
  margin-top: -26%;
  margin-right: 25%;

  &:before {
    display: block;
    content: '';
    padding-bottom: 98%;
  }
  img {
    position: absolute;
    width: 100%;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
  }
}

@media (max-width: 800px) {
  .men_main {
    justify-content: start;
  }

  .men_image {
    margin: -36% 0 0;
    width: 48%;
  }
}
</style>
