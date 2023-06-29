<template>
  <div class="container">

    <div class="menu-bar">

      <img src="@/assets/logo.png" alt="">

      <div class="menu-container">
        <a href="">자전거</a>
        <a href="">용품</a>
        <a href="">매장안내</a>
        <a href="">LIV커뮤니티</a>
        <a href="">가이드</a>
        <a href="">온라인구매</a>
      </div>

      <div class="search-bar">
        <input type="text" placeholder="여기에 검색해보세요">
        <span>🌐</span>
      </div>
    </div>

    <div class="banner" v-if="openBanner">
      <p>여성용 레이스 바이크</p> <a href="https://www.liv-cycling.com/kr/enviliv">신형 엔비리브 출시</a>
      <button @click="$emit('closeBanner','')">닫기</button>
    </div>

  </div>

</template>

<script>
export default {
  name: 'Menu',
  props:{
    openBanner: Boolean,
  }
}
</script>

<style>
.container{
  position:fixed;
  top:0;
  width: 100%;
}

.menu-bar{
  background: white;
  width:100%;
  height: 50px;
  padding: 20px;
  align-items: center;
  display: flex;
  border-bottom: 1px solid rgb(220,220,220);
}
.menu-bar img{
  height: 80%;
  margin-right: auto;
}

.menu-bar a{
  padding: 20px;
  text-decoration: none;
  color: purple;
}

.search-bar{
  margin-left: auto;
  padding: 0 5vw 0 5vw;
}
.search-bar input{
  border: none;
  text-align: center;
  border-bottom: 1px solid rgb(220, 220, 220);
}


.banner{
  background:rgba(211, 211, 211, 0.85);
  width: 100%;
  display: flex;
  height: 50px;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

</style>