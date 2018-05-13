<template lang="html">
    <div>
    <v-index></v-index>
  <div class="wrapper">
    <div class="intr">
        <div class="timer">
            <img src="../public/icons/dengji.png" alt="">
            <span @click="intrshow">0分钟</span>
        </div>
        <div class="avatar" @click="intrshow">
            <img src="../public/icons/avatar.jpg" alt="">
            <transition name="fold">
                <div class="intr1" v-show="intrShow">
                    <div>阿兰&阿雨<br/>给岁月以爱情，给我们以岁月</div>
                </div>
            </transition>
        </div>
        <div class="vip">
            <img src="../public/icons/vvip.png" alt="">
            <span @click="intrshow">开通</span>
        </div>
    </div>
    <p class="username" @click="intrshow">{{username}}</p>
    <div class="intr-songs">
        <div class="t-intr-songs">
            <div class="t-intr-songs1">
                <router-link to="/total">
                <img src="../public/icons/yinfu.png" alt="">
                <p>全部歌曲</p>
                </router-link> 
            </div>
            <div class="t-intr-songs1">
                <router-link to="/download">
                <img src="../public/icons/download.png" alt="">
                <p>下载歌曲</p>
                </router-link>
            </div>
            <div class="t-intr-songs1">
                <router-link to="/musiclist">
                <img src="../public/icons/zuijin.png" alt="">
                <p>最近播放</p>
                </router-link>
            </div>       
        </div>
        <div class="b-intr-songs">
            <div class="b-intr-songs1">
                <img src="../public/icons/heart.png" alt="">
                <p>我喜欢</p>
                <small></small>
            </div>
            <div class="b-intr-songs1">
                <img src="../public/icons/mv.png" alt="">
                <p>下载MV</p>
            </div>
            <div class="b-intr-songs1">
                <img src="../public/icons/cd.png" alt="">
                <p>已购音乐</p>
            </div>
        </div>
    </div>
    <div class="blank"></div>
  </div>
  <div class="radio">
      <div class="radio1">
        <img src="../public/icons/run.jpg" alt="">
        <!--<img src="" alt="">-->
        <div class="title">
        <p>个性电台</p>
        <small>听 Seve 的人也喜欢听这些歌曲</small>
        </div>
      </div>
      <div class="radio2">
        <img src="../public/icons/run1.jpg" alt="">
        <!--<img src="" alt="">-->
        <div class="title2">
        <p>NIKE跑步电台</p>
        <small>新增万首中文跑步歌曲,点燃你的2017</small>
        </div>
      </div>
  </div>
  <div class="blank1"></div>
  <div class="songlist">
      <p class="title">我 的 歌 单 </p>
  </div>
  <router-link to="/like">
  <div class="list" >
      <img src="../public/icons/jay1.jpg" alt="">
      <div class="number">
          <p>雨田MUSIC</p>
          <small></small>
      </div>
  </div>
    <div class="list">
      <img src="../public/icons/jay1.jpg" alt="">
      <div class="number">
          <p>雨田MUSIC</p>
          <small></small>
      </div>
  </div>
  </router-link>
  <div class="blank2">
      
  </div>
  </div>
</template>

<script>
import index from '@/components/index.vue'
export default {
    data () {
        return {
            intrShow: false,
            username: '雨田'
        }
    },
    components: {
        "v-index": index
    },
    methods: {
      intrshow () {
         this. intrShow = ! this.intrShow
      }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/header.scss';
.intr1{
    display: flex;
    justify-content: center;
    align-items: center;
    div{
        font-size: 56px;
        display: block;
    }
}
</style>