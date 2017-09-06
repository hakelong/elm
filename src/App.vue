<template>
  <div id="app">
      <myheader></myheader>
      <div class='tab'>
          <div class='tab-item'><router-link to='/goods' >商品</router-link></div>
          <div class='tab-item'><router-link to='/ratings'>评论</router-link></div>
          <div class='tab-item'><router-link to='/seller'>商家</router-link></div>
      </div>
      <div class='content'>
        <router-view></router-view>
      </div>
  </div>
</template>

<script>
import myheader from './components/header/header.vue'

export default {
  name: 'app',
  components: {
    myheader
  }
}
</script>

<style >
    #app .tab{
      display: flex
    }
    #app .tab .tab-item{
      flex: 1;
      text-align:center;
    }
     #app .tab .tab-item a{
      display: block;
      text-decoration:none;
      font-size: 14px;
      color: rgb(77,85,93);
    }
    #app .tab .tab-item a.active{
      color:rgb(240,20,20);
    }
</style>
