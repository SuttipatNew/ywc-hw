<template>
  <div class="sponsors">
    <div class="sponsor" v-for="image in images" :key="image">
      <img :src="image" />
    </div>
  </div>
</template>

<script>
import mof_img from '../assets/images/brand-logo/MOF.png'
import fpo_img from '../assets/images/brand-logo/FPO.png'
import cgd_img from  '../assets/images/brand-logo/CGD.png'
import ktb_img from '../assets/images/brand-logo/Krungthai.png'
import mots_img from '../assets/images/brand-logo/MOTS.png'
import tat_img from '../assets/images/brand-logo/TAT.png'

export default {
  name: 'Sponsors',
  data() {
    return {
      images: [
        mof_img,
        fpo_img,
        cgd_img,
        ktb_img,
        mots_img,
        tat_img
      ]
    }
  }
}
</script>

<style scoped>

.sponsors {
  grid-column: span 12;
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-column-gap: 15px;
}

.sponsor {
  text-align: center;
}

.sponsors img {
  width: 120px;
}

</style>
