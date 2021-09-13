<template>
  <div :class="$style.footer_main">
    <div :class="$style.max_size">
      <div :class="$style.footer_boxs">
        <div :class="$style.logo">
          <div :class="$style.logo_img">
            <img src="@/assets/imgs/logo33.png" />
          </div>
          <a href="mailto:food@gmail.com"
            ><img src="@/assets/imgs/email.png" /> food@gmail.com</a
          >
          <a href="tel:(909) 303-1234"
            ><img src="@/assets/imgs/tel2.png" />(909) 303-1234</a
          >
        </div>
      </div>
      <div :class="$style.menobar">
        <div v-for="(i, id) in list" :key="id" :class="$style.meno_box">
          <div :class="$style.menobar_title">{{ i.title }}</div>
          <div
            v-for="(item, p_id) in i.page"
            :key="p_id"
            :class="$style.menobar_page"
          >
            {{ item }}
          </div>
        </div>
      </div>
      <div :class="$style.footer_boxs">
        <div :class="$style.menobar_title">Subscribe Us</div>
        <div :class="$style.search_box">
          <input type="text" placeholder="Enter Email Address" />
          <div :class="$style.send_btn">Send</div>
        </div>
        <div :class="$style.social">
          <img src="@/assets/imgs/facebook.png" />
          <img src="@/assets/imgs/instagram.png" />
          <img src="@/assets/imgs/twitter.png" />
          <img src="@/assets/imgs/youtube.png" />
        </div>
      </div>
    </div>
    <div :class="$style.copy_right_2">Deliveright, 2021 Allright reserved</div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    list: [
      {
        title: 'Responses',
        page: ['How it work', 'Guarantee', 'Security', 'Pricing'],
      },
      {
        title: 'About',
        page: ['Policy', 'Jobs', 'Testimonils', 'Blogs'],
      },
    ],
  }),
}
</script>

<style lang="scss" module>
.footer_main {
  background: linear-gradient(90deg, #525fe1 0%, #525fe1 49%, #5966e9 100%);
}

.max_size {
  max-width: 1200px;

  margin: 0 auto;
  display: flex;
  padding: 10% 15px 7%;
}

.footer_boxs,
.menobar {
  width: 50%;
  overflow: hidden;
}

.menobar {
  display: flex;
  justify-content: space-around;
}

.logo {
  a {
    display: block;
    color: #d3d7f8;
    margin-bottom: 6%;
    transition: all 0.3s ease;
    img {
      width: 30px;
      vertical-align: bottom;
      margin-left: 1%;
      margin-right: 3%;
    }
    &:hover {
      opacity: 0.7;
    }
  }
}

.logo_img {
  position: relative;
  width: 30%;
  padding-bottom: 13%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 58%;
  }
  img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
  }
}

.copy_right_2 {
  display: none;
  text-align: center;
  font-weight: 600;
  padding: 2% 0;
  background: #a1b0ff;
}

.meno_box {
  width: 30%;
}

.menobar_title {
  font-size: 19px;
  font-weight: 500;
  margin-bottom: 15%;
  color: #fff;
}

.menobar_page {
  line-height: 3;
  font-weight: 500;
  transition: all 0.3s ease;
  cursor: pointer;
  color: #d4d7f0;
  &:hover {
    opacity: 0.7;
  }
}

.search_box {
  width: 75%;
  border: 1px solid #d3d7f8;
  display: flex;
  justify-content: space-between;
  border-radius: 5px;

  input {
    background: none;
    font-size: 17px;
    width: 80%;
    border: none;
    padding: 5%;
    color: #d3d7f8;

    &:focus {
      outline: none;
    }
  }
}

.send_btn {
  background: #d3d7f8;
  width: 25%;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
  color: #313416;
  transition: all 0.3s ease;
  cursor: pointer;
  &:hover {
    opacity: 0.7;
  }
}

.social {
  display: flex;
  margin-top: 8%;
  img {
    width: 5%;
    display: block;
    margin-right: 10%;
    cursor: pointer;
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
  }
}

@media (max-width: 800px) {
  .max_size {
    flex-direction: column-reverse;
  }

  .menobar_title {
    text-align: center;
    margin-bottom: 5%;
  }

  .search_box {
    margin: 0 auto;
  }

  .social {
    margin: 8% 0;
    justify-content: center;
  }

  .footer_boxs {
    margin: 7% auto 0;
    width: 80%;
  }

  .menobar {
    width: 80%;
    margin: 0 auto;
    text-align: center;
  }

  .logo a {
    text-align: center;
  }

  .logo_img {
    margin: 0 auto;
  }

  .copy_right_2 {
    display: block;
  }
}

@media (max-width: 600px) {
  .menobar_title {
    font-size: 16px;
  }

  .menobar_page {
    font-size: 14px;
  }
}

@media (max-width: 450px) {
  .menobar_title {
    font-size: 20px;
  }

  .menobar_page {
    font-size: 16px;
  }

  .menobar {
    flex-direction: column;
  }

  .meno_box {
    width: 100%;
    text-align: center;
  }
}
</style>
