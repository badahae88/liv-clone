<template>
  <div class="Card">
    <h1>{{item.title}}</h1>
    <p>{{item.price}}원</p>
    <img :src="item.image" alt="{{item.title}}사진">
  </div>
</template>

<script>
export default {
  name: 'Card',
  data(){
    return{

    }
  },
  props: {
    item: Object,
  }

}
</script>

<style>
.Card{
  background: white;
  width: 50%;
  max-width: 700px;
  box-shadow: rgba(100, 100, 100, 0.2) 0px 7px 29px 0px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  padding-bottom: 20px;
  margin: 150px auto;
}
.Card img{
  width: 80%;
}
</style>