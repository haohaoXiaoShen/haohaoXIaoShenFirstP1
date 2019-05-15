<template>
  <div id="NowPlaying">
    <ul>
      <li v-for="(item,index) in playList" :key="index">
        <img :src="item.pic_url" alt>
        <span class="title">{{item.movieName}}</span>

        <span class="des">{{item.movieId}}</span>
        <img src="../../../public/icon/热度.png" alt class="hot">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "NowPlaying",
  data() {
    return {
      playList: []
    };
  },
  created() {
    this.axios(
      "/apiNowPlay/movie/movies.today?key=189f5076a3940ca59bd8990cd5c65742&cityid=3"
    ).then(res => {
      console.log(res.data.result);
      this.playList = res.data.result;
    });
  }
};
</script>

<style scoped>
li {
  padding: 13px;
  border-bottom: 1px solid rosybrown;
  position: relative;
}
img {
  width: 35%;
  display: inline-block;
  vertical-align: top;
}
.title {
  padding: 15px;
  font-size: 20px;
}
.des {
  background-color: rgba(191, 218, 40, 0.753);
  padding: 2px;
  border: rgba(7, 29, 48, 0.534) 1px solid;
  font-size: 5px;
  font-weight: bold;
}
.hot {
  width: 30px;
  position: absolute;
  top: 12px;
  right: 10px;;
}
</style>
