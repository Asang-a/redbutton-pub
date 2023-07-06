<template>
  <div class="footer">
    <div class="footer-contents">
      <img class="logo" src="../assets/image/logo.png" />
    </div>
    <div class="footer-contents center">
      <span class="icon-home on"></span>
      <span class="icon-dice"></span>
      <span class="icon-home"></span>
    </div>
    <div class="footer-contents">
      <button class="btn-circle">제보</button>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<script lang="ts">
export default {}
</script>

<style lang="scss">
.footer {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: $achromatic0;
  height: 108px;
  border-top: 1px solid $achromatic40;
  padding: 0 50px;
}

.footer-contents {
  width: 20%;
  &:last-child {
    text-align: right;
  }

  &.center {
    width: auto;
    display: flex;
    justify-content: center;
    > span {
      margin: 0 55px;
    }
    > .on {
      color: $highlight;
    }
  }
}

.logo {
  width: auto;
  height: 45px;
}

.icon-home {
  display: inline-block;
  background-image: url('/src/assets/image/icon-home.svg');
  background-repeat: no-repeat;
  background-size: contain;
  width: 50px;
  height: 50px;
}
.icon-dice {
  display: inline-block;
  background-image: url('/src/assets/image/icon-dice.svg');
  background-repeat: no-repeat;
  background-size: contain;
  width: 50px;
  height: 50px;
}

.btn-circle {
  width: 55px;
  height: 55px;
  padding: 0;
  border: 1px solid $achromatic55;
  border-radius: 50%;
  background-color: rgba(0, 0, 0, 0);
  font-size: 26px;
  color: $achromatic50;
}
</style>
