<template>
  <div :class="$style.header_main">
    <div :class="$style.max_size">
      <Header />
      <div :class="$style.sofa_boxs">
        <div :class="$style.boxs">
          <div :class="$style.title">
            Get your food Delivery at your Doorstep
          </div>
          <div :class="$style.description">
            You can get scooter hourly and monthly plus yearly basis We have
            many scooter nearby your location.
          </div>
          <div :class="$style.btns">
            <div :class="$style.buy">Order Now</div>
            <div :class="$style.explore">Track your order</div>
          </div>
        </div>
        <div :class="$style.boxs">
          <div :class="$style.frame_image">
            <img src="@/assets/imgs/style2.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './Header/Header.vue'
export default {
  name: 'HeaderMain',
  components: {
    Header,
  },
}
</script>

<style lang="scss" module>
.header_main {
  background: #525fe1;
  color: #fff;
}

.max_size {
  max-width: 1200px;
  padding-left: 15px;
  padding-right: 15px;
  margin: 0 auto;
}

.sofa_boxs {
  display: flex;
  margin-top: 4%;
}

.boxs {
  width: 50%;
}

.title {
  font-weight: 600;
  font-size: 59px;
  margin-right: 18%;
  line-height: 1;
}

.description {
  margin: 5% 16% 7% 0;
}

.btns {
  display: flex;
  margin-bottom: 13%;
}

.buy {
  background: #f67001;
  padding: 3% 6.7%;
  margin-right: 3%;
}

.explore {
  border: 1px solid #fff;
  padding: 3% 5%;
}

.buy,
.explore {
  font-weight: 600;
  border-radius: 50px;
  transition: all 0.3s ease;
  cursor: pointer;
  &:hover {
    opacity: 0.8;
  }
}

.frame_image {
  position: relative;
  width: 96%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 77%;
  }
  img {
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
}

@media (max-width: 800px) {
  .sofa_boxs {
    flex-direction: column;
  }

  .boxs {
    width: 100%;
  }

  .title {
    margin: 0 10% 10%;
  }

  .description {
    display: none;
  }

  .btns {
    display: none;
  }

  .frame_image {
    width: 78%;
    margin: 0 auto;
  }
}

@media (max-width: 600px) {
  .title {
    font-size: 50px;
  }
}

@media (max-width: 450px) {
  .title {
    font-size: 33px;
  }
}
</style>
