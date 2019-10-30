<template>
  <div id="app">
    <Navbar :items="navbarItems" />
    <Banner />
    <p id="pre-duration" class="text-center">ตั้งแต่วันที่</p>
    <p id="duration" class="text-center">{{ duration }}</p>
    <Register />
    <div class="container">
      <div class="content-wrapper">
        <h2>มาตรการส่งเสริมการบริโภค</h2>
        <h2>
          ในประเทศ
          <span class="nowrap">
            “ชิมช้อปใช้”
          </span>
        </h2>
        <div class="detail">
          <p v-html="detail">
          </p>
        </div>
        <div class="condition">
          <h3>เงื่อนไขการเข้าร่วมมาตรการ</h3>
          <p v-html="condition">
          </p>
        </div>
      </div>
      <Call />
      <Sponsors />
    </div>
    <FootMenu />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Banner from './components/Banner.vue'
import Register from './components/Register.vue'
import Call from './components/Call.vue'
import Sponsors from './components/Sponsors.vue'
import FootMenu from './components/FootMenu'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    Navbar,
    Banner,
    Register,
    Call,
    Sponsors,
    FootMenu,
    Footer
  },
  data() {
    return {
      duration: null,
      navbarItems: [
      ],
      detail: null,
      condition: null
    }
  },
  mounted() {
    fetch("https://panjs.com/ywc.json").then(res => {
      res.json().then(data => {
        for (let key in data) {
          this[key] = data[key]
        }
      })
    })
  }
}
</script>

<style>
@font-face {
  font-family: 'TATSanaChon';
  src: url('./assets/fonts/TATSanaChon-Regular.woff2');
}

@font-face {
  font-family: 'TATSanaSuksa';
  src: url('./assets/fonts/TATSanaSuksa-Regular.woff2');
}

@font-face {
  font-family: 'TATSanaSuksaBold';
  src: url('./assets/fonts/TATSanaChon-Bold.woff2');
}

body {
  margin: 0;
  font-family: TATSanaSuksa;
  color: #333333;
}

p {
  margin: 0;
}

a {
  text-decoration: none;
  color: inherit;
}

h2 {
  margin: 0;
  font-family: TATSanaSuksaBold;
  color: #E6332A;
  font-size: 36px;
  line-height: 1.6;
}

h3 {
  margin: 0;
  font-family: TATSanaSuksaBold;
  font-size: 18px;
}

.container {
  width: 100%;
  padding: 0px 15px;
  margin-left: auto;
  margin-right: auto;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-column-gap: 15px;
}
@media (min-width: 576px) {
  .container {
    max-width: 540px;
  }
}
@media (min-width: 768px) {
  .container {
    max-width: 720px;
  }
}
@media (min-width: 992px) {
  .container {
    max-width: 960px;
  }
}
@media (min-width: 1200px) {
  .container {
    max-width: 1140px;
  }
}

.nowrap {
  white-space: nowrap;
}

.text-center {
  text-align: center;
}

.content-wrapper {
  grid-column: span 10;
}

#pre-duration {
  font-size: 16px;
  font-family: TATSanaSuksaBold;
  margin-top: 26px;
}

#duration {
  margin-top: -10px;
  color: #E6332A;
  font-size: 48px;
  font-family: TATSanaSuksaBold;
}

.detail {
  margin-top: 1.5rem;
  font-size: 18px;
}

.condition {
  margin-top: 1.5rem;
  font-size: 18px;
}

.condition p {
  margin-top: 0.5rem;
}
</style>
