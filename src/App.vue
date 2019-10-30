<template>
  <div id="app">
    <Navbar :items="navbarItems" />
    <div class="container">
      <p id="pre-duration" class="text-center">ตั้งแต่วันที่</p>
      <p id="duration" class="text-center">{{ duration }}</p>
      <h2>มาตรการส่งเสริมการบริโภค</h2>
      <h2>ในประเทศ “ชิมช้อปใช้”</h2>
      <p v-html="detail">
      </p>
      <h3>เงื่อนไขการเข้าร่วมมาตรการ</h3>
      <p v-html="condition">
      </p>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    Navbar,
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

body {
  margin: 0;
  font-family: TATSanaSuksa;
  color: #333333;
}

p {
  margin: 0;
}

h2 {
  margin: 0;
}

.container {
  margin-top: 60px;
  padding: 0px 15px;
}

.text-center {
  text-align: center;
}

#pre-duration {
  font-size: 16px;
  font-weight: bold;
  font-family: TATSanaSuksa;
}

#duration {
  margin-top: -10px;
  color: #E6332A;
  font-size: 48px;
  font-weight: bold;
  font-family: TATSanaSuksa;
}
</style>
