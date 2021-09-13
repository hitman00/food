<template>
  <div :class="$style.slider_main">
    <div :class="$style.slide_text">
      <div :class="$style.title">Why we are best in our Town</div>
      <div :class="$style.description">
        We have 5000+ Review and our customers trust on our food and Deliver
        service. You can read more about our company.
      </div>
      <div :class="$style.btn">
        <img src="@/assets/imgs/arrow.png" />
      </div>
    </div>
    <div :class="$style.slide_items">
      <div
        v-for="(i, id) in list"
        :key="id"
        :class="[$style.boxs, id == 1 ? $style.resize : '']"
      >
        <div :class="$style.slider_image">
          <img :src="i.img" />
        </div>
        <div :class="$style.slider_title">{{ i.title }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data() {
    return {
      list: [
        {
          img: require('@/assets/imgs/rice.png'),
          title: 'Choses Your favorite Food',
        },
        {
          img: require('@/assets/imgs/motor.png'),
          title: 'Get delivery At your dood step',
        },
        {
          img: require('@/assets/imgs/hand1.png'),
          title: 'We have 5000+ Review On our app',
        },
      ],
    }
  },
}
</script>

<style lang="scss" module>
.slider_main {
  display: flex;
  margin-top: 5%;
}

.slide_text {
  width: 25%;
}

.title {
  font-size: 40px;
  font-weight: 600;
  line-height: 1.3;
}

.description {
  font-weight: 200;
  margin-top: 15%;
  margin-bottom: 22.7%;
}

.btn {
  width: 55px;
  height: 55px;
  background: #f67001;
  border-radius: 50%;
  margin-left: 10%;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.3s ease;
  cursor: pointer;
  img {
    width: 54%;
  }
  &:hover {
    opacity: 0.8;
  }
}

.slide_items {
  width: 75%;
}

.boxs {
  width: 28%;
  border-radius: 30px;
  float: left;
  margin: 0 2.5%;
  padding: 3% 2%;
  box-shadow: 0px 3px 15px #c7c9c8;
  transition: all 0.4s ease;
  cursor: pointer;
  &:hover {
    background: #f6f6f6;
  }
  &.resize {
    margin-top: 11%;
  }
}

.slider_image {
  position: relative;
  width: 77%;
  margin: 0 auto;
  &:before {
    content: '';
    display: block;
    padding-bottom: 100%;
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

.slider_title {
  font-weight: 600;
  font-size: 18px;
  margin: 31% 24% 32% 15%;
}

@media (max-width: 800px) {
  .slider_main {
    flex-direction: column;
    margin-top: 9%;
  }

  .slide_text,
  .slide_items {
    width: 80%;
    margin: 0 auto;
  }

  .description {
    margin: 6% 0;
  }

  .btn {
    margin: 0 auto 2%;
  }

  .slider_title {
    margin: 18% 3% 11%;
    font-size: 15px;
  }
}

@media (max-width: 600px) {
  .slider_title {
    font-size: 12px;
  }
}

@media (max-width: 450px) {
  .title {
    font-size: 30px;
  }

  .slide_items {
    flex-direction: column;
  }

  .slider_title {
    font-size: 18px;
  }

  .boxs {
    width: 80%;
    margin: 15% auto;
    float: none;
    &.resize {
      margin-top: 0%;
    }
  }

  .slider_image {
    width: 51%;
    margin-top: 7.5%;
  }
}
</style>
