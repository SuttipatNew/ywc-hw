<template>
  <div class="register">
    <a href="https://regist.xn--b3caa1e2a7e2b0h2be.com/Register/">
      <button id="register-button">
        <span>ลงทะเบียนเฟส 2</span>
        <br />
        <span>ตั้งแต่วันที่ 24 ต.ค. 62 วันละ 2 รอบ เวลา 6.00 และ 18.00 น.</span>
        <br />
        <span>(จำกัดจำนวนผู้ลงทะเบียนรอบละ 5 แสนคน รวม 1 ล้านคนต่อวัน)</span>
      </button>
    </a>
    <hr />
  </div>
</template>

<script>
export default {
  name: 'Register'
}
</script>

<style scoped>
.register {
  padding: 0px 15px;
  text-align: center;
  margin-bottom: 95px;
}

hr {
  color: rgba(0, 0, 0, 0.0980392);
  border-width: 1px 0px 0px;
  border-top: 1px solid rgba(0, 0, 0, 0.0980392);
  height: 0px;
  width: 100%;
  margin-top: -25px;
}

button {
  line-height: 1.4;
  cursor: pointer;
  padding: 15px 50px;
  display: inline-block;
  text-align: center;
  overflow: visible;
  height: auto;
  font-size: 24px;
  border: 0px;
  background-color: rgb(33, 58, 143);
  color: white;
  border-radius: 5px;
  font-family: TATSanaSuksaBold;
  box-shadow: rgba(28, 78, 132, 0.4) 0px 15px 30px 0px;
  outline: none;
  transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
}

button:hover {
  background-color: #FBBC33;
  box-shadow: none;
}

@media (max-width: 577px) {
  button {
    font-size: 18px;
    padding: 10px;
    margin: 10px 0;
  }
}

</style>
