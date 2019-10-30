<template>
  <div class="banner">
    <div
      class="banner-item" 
      v-for="index in 3" 
      :key="index"
      :style="`background-image: url(${bannerBgs[index - 1]});`"
    >
      <img id="banner-logo" :src="logo" v-if="index == 2" />
    </div>
  </div>
</template>

<script>
import bg1 from '../assets/images/banner-left.png'
import bg2 from '../assets/images/banner-center.png'
import bg3 from '../assets/images/banner-right.png'
import logo from '../assets/images/banner.png'

export default {
  name: 'Banner',
  data() {
    return {
      bannerBgs: [
        bg1,
        bg2,
        bg3
      ],
      logo: logo
    }
  }
}
</script>

<style scoped>

.banner {
  margin-top: 60px;
  position: relative;
  height: 350px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.banner-item {
  height: 100%;
  background-size: cover;
  text-align: center;
  line-height: 350px;
}

#banner-logo {
  vertical-align: middle;
}

</style>
