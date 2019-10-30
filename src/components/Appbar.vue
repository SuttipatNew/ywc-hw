<template>
  <div class="appbar">
    <img :src="logo" />
    <button class="hamburger">
      =
    </button>
  </div>
</template>

<script>
import logo from '../assets/images/footer.png'
export default {
  name: 'Appbar',
  data() {
    return {
      logo
    }
  }
}
</script>

<style scoped>
.appbar {
  height: 60px;
  box-sizing: border-box;
  position: fixed;
  z-index: 11;
  padding: 8px 16px;
  width: 100vw;
  background-color: white;
  top: 0;
  display: flex;
  justify-content: space-between;
}

@media (min-width: 578px) {
  .appbar {
    display: none;
  }
}

img {
  display: block;
  width: 35px;
  height: 48px;
}

.hamburger {
  cursor: pointer;
}
</style>
