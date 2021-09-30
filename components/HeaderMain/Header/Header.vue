<template>
  <div :class="$style.header_top_main">
    <div :class="$style.logo">Deliveright</div>
    <div :class="$style.menobar">
      <ul>
        <li>Home</li>
        <li>About us</li>
        <li>Services</li>
        <li>Blog</li>
        <li>Contact us</li>
        <li><a href="https://hitman00.github.io/food/">Github</a></li>
      </ul>
      <img src="@/assets/imgs/menoba.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss" module>
.header_top_main {
  width: 100%;
  display: flex;
  padding: 5% 0;
}

.logo {
  width: 20%;
  font-weight: 500;
  font-size: 34px;
}

.menobar {
  width: 80%;
  font-weight: 600;
  position: relative;
  ul {
    display: flex;
    justify-content: end;
    li {
      padding: 1% 2%;
      transition: all 0.3s ease;
      border-radius: 50px;
      cursor: pointer;
      a {
        color: #fff;
      }
      &:hover {
        background: #f67001;
      }
    }
  }
  img {
    display: none;
    width: 30px;
    position: absolute;
    right: 0;
    margin-top: 2%;
  }
}

@media (max-width: 800px) {
  .header_top_main {
    width: 85%;
    margin: 0 auto;
  }

  .logo {
    font-weight: 600;
    font-size: 30px;
  }

  .menobar {
    ul {
      display: none;
    }
    img {
      display: block;
    }
  }
}

@media (max-width: 450px) {
  .logo {
    font-size: 25px;
  }
}
</style>
