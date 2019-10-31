<template>
  <div class="banner">
    <div
      :class="'banner-item banner-item-' + index" 
      v-for="index in 3" 
      :key="index"
    >
      <img id="banner-logo" :src="logo" v-if="index == 2" />
    </div>
  </div>
</template>

<script>
import logo from '../assets/images/banner.png'

export default {
  name: 'Banner',
  data() {
    return {
      logo: logo
    }
  }
}
</script>

<style scoped>

.banner {
  margin-top: 60px;
  position: relative;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.banner-item {
  height: 100%;
  background-size: cover;
  text-align: center;
  line-height: 350px;
  height: 350px;
}

.banner-item-1 {
  background-image: url('../assets/images/banner-left.png');
}
.banner-item-2 {
  background-image: url('../assets/images/banner-center.png');
}
.banner-item-3 {
  background-image: url('../assets/images/banner-right.png');
}

#banner-logo {
  vertical-align: middle;
  width: 240px;
}

@media (max-width: 769px) {
  .banner-item {
    height: 242px;
    line-height: 242px;
  }
  #banner-logo {
    width: 146px;
    height: 173px;
  }
  .banner-item-1 {
    background-image: url('../assets/images/banner-left-s.png');
  }
  .banner-item-2 {
    background-image: url('../assets/images/banner-center-s.png');
  }
  .banner-item-3 {
    background-image: url('../assets/images/banner-right-s.png');
  }
}

@media (max-width: 577px) {
  .banner-item {
    height: 221px;
    line-height: 221px;
  }
  #banner-logo {
    width: 110px;
    height: 131px;
  }
}


</style>
