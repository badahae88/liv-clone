<template>
  <div class="black-bg" v-if="showModal">
    <div class="white-bg">
      <h2>{{showItem.title}}</h2>
      
      <h3>가격: {{ showItem.price }}원 </h3>

      <div class="input-wrapper">
        <p>사이즈 선택 : </p>
        <select v-model="size">
          <option v-for="size in showItem.sizes" :key="size">{{size}}</option>
        </select>
      </div>

      <div class="input-wrapper">
        <p>할부기간 : {{month}}</p>
        <input v-model.number="month" type="range" min="1" max="12">
      </div>

      <p>{{size}}사이즈 {{month}}개월 할부</p>
      <h3>🔥 월 {{Math.round(showItem.price/month)}}원 납부 🔥</h3>
      <a :href="showItem.details">❓자세히 알아보기❓</a>

      <button @click="$emit('closeModal','')">닫기</button>

    </div>

  </div>
</template>

<script>
export default {
  name: "Modal",
  data(){
    return {
      size:'m',
      month:12,
    };
  },
  props: {
    showModal: Boolean,
    showItem: Object,
  }
}
</script>

<style>
.black-bg{
  width:100%; height:100%;
  background: rgba(0, 0, 0, 0.5);
  position:fixed;
  z-index:9999999999999999;
}
.white-bg{
  position: fixed;
  top: 20vh; left: 28vw;
  width: 40%;
  background: white;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.input-wrapper{
  display: flex;
  align-items: center;
}
.input-wrapper input {
  margin-left: 10px;
}
.input-wrapper select {
  margin-left: 10px;
  border: none;
  background: rgba(128, 0, 128, 0.481);
  color: white;
}
.white-bg a{
  text-decoration: none;
  margin-bottom: 15px;
  color: purple;
  font-weight:bold;
}
.white-bg button{
  border: none;
  width: 20%;
  background: rgba(128, 0, 128, 0.481);
  color: white;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  
}
</style>