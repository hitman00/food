<template>
  <div :class="$style.getstart_main">
    <div :class="$style.max_size">
      <div :class="$style.title">Want to try our service?</div>
      <div :class="$style.description">
        We are offering free debit cards once you sign up and order a card. We
        won't change you for our debit card and wallet for the first year.
      </div>
      <div :class="$style.btn">Get Started</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GetStart',
}
</script>

<style lang="scss" module>
.getstart_main {
  margin-top: 3%;
  color: #fff;
  width: 100%;
  background: #6773e5;
}

.max_size {
  max-width: 1200px;
  padding-left: 15px;
  padding-right: 15px;
  margin: 0 auto;
  padding: 6% 9%;
  text-align: center;
  color: #dee2ff;
}

.title {
  font-weight: 600;
  font-size: 45px;
  line-height: 1.2;
}

.description {
  font-weight: 300;
  margin: 3% 0;
  font-size: 20px;
}

.btn {
  background: #7c87e9;
  padding: 2% 4%;
  margin: 0 auto;
  font-size: 18px;
  border-radius: 50px;
  color: #fff;
  display: inline-block;
  cursor: pointer;
  transition: all 0.3s ease;
  border: 10px inset #202eac;
  &:hover {
    opacity: 0.8;
  }
}

@media (max-width: 800px) {
  .max_size {
    flex-direction: column;
  }
}

@media (max-width: 600px) {
  .title {
    font-size: 30px;
  }
}

@media (max-width: 450px) {
  .title {
    font-size: 25px;
  }
}
</style>
