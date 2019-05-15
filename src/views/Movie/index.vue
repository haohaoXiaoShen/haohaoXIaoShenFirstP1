<template>
  <div id="Movie">
    <Header></Header>
    <div class="content">
      <ul>
        <router-link tag="li" to="/movie/city">
         <img src="../../../public/icon/定位.png" alt="">
          <span>广州</span>
         
        </router-link>
        <router-link tag="li" to="/movie/nowPlaying">正在热映</router-link>
        <router-link tag="li" to="/movie/commingsoon">即将上映</router-link>
        <router-link tag="li" to="/movie/search">
          <img src="../../../public/icon/搜索.png" alt>
        </router-link>
      </ul>
    </div>
    <Footer></Footer>

    <keep-alive>
      <router-view></router-view>
    </keep-alive>
  </div>
</template>

<script>
import Header from "@/components/Header";
import Footer from "@/components/Tabbar";
export default {
  name: "Movie",
  components: {
    Header,
    Footer
  }
};
</script>

<style scoped>
ul {
  display: flex;
}
li {
  flex: 4;
  text-align: center;
  height: 50px;
  line-height: 50px;
}
img {
  width: 25px;
  display: inline-block;
  margin-top: 5px;
  vertical-align:-8px;
}
.router-link-active {
  border-bottom: 2px solid rgba(211, 46, 46, 0.555);
}
</style>
