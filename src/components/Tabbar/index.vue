<template>
  <footer id="footer">
    <ul>
      <router-link to="/movie" tag="li">
        <img src="../../../public/icon/电影.png" alt>
        <p>电影</p>
      </router-link>
      <router-link to="/cinema" tag="li">
      <img src="../../../public/icon/影院.png" alt>
        <p>影院</p>
      </router-link>
      <router-link to="/mine" tag="li">
      <img src="../../../public/icon/我的.png" alt>
        <p>我的</p>
      </router-link>
    </ul>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
#footer {
  width: 100%;
  height: 70px;
  background: white;
  border-top: 2px #ebe8e3 solid;
  position: fixed;
  left: 0;
  bottom: 0;
}
ul{
  display: flex;
  height: 100%;
}
li{
  flex: 3;
  text-align: center
}
img{
  width: 40px;
  text-align: center;
  display: inline-block;
  
}
.router-link-active{
  background-color: rgba(245, 245, 220, 0.431);
  color: red;
  border-bottom: 1px solid rgba(91, 91, 131, 0.226)
}
</style>
