<template>
  <div class="nav">
    <router-link to="./foods">商品</router-link>
    <router-link to="./rating">评价 ({{comment_num}})</router-link>
    <router-link to="./seller">卖家信息</router-link>
  </div>
</template>

<script>
export default {
  // name: 'nav',
  data(){
    return {}
  },
  props: {
    comment_num:{
      type: Number,
      default: 0
    },
      
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav{
  display: flex;
  justify-content: space-around;
  height: 40px; 
  border-bottom: 1px solid #ddd;
}
a{
  position: relative;
  height: 40px; 
  line-height: 40px;
  font-size: 14px;
  text-decoration: none;
  color: #424242;
}
.router-link-active{
  color: #fd2
}
a.router-link-active::after{
  position: absolute;
  left: 50%;
  bottom: -1px;
  content: '';
  display: inline-block;
  width: 100%;
  margin-left: -50%;
  border-bottom: 2px solid #fd2;
}
</style>