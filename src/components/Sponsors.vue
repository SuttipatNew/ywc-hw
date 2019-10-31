<template>
  <div class="sponsors">
    <div class="sponsor" v-for="(image, index) in images" :key="image">
      <a :href="urls[index]">
        <img :src="image" />
      </a>
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
      ],
      urls: [
        'https://www.mof.go.th/th/home',
        'http://www.fpo.go.th',
        'https://www.cgd.go.th',
        'https://www.newcb.ktb.co.th',
        'https://www.mots.go.th',
        'https://thai.tourismthailand.org'
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
}

@media (max-width: 767px) {
  .sponsors {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 426px) {
  .sponsors {
    padding: 0 10%;
  }
}

.sponsor {
  text-align: center;
}

.sponsors img {
  width: 120px;
}

@media (max-width: 426px) {
  .sponsors img {
    width: 56px;
  }
}

</style>
