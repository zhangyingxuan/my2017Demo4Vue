<template>
  <mt-swipe :auto="0">
    <mt-swipe-item class="swip-item-2 item">
      <header class="page6_header">
        <img class="page6_header_moon_img" src="../assets/6/moon.png"/>
        <img class="page6_header_star1_img" src="../assets/6/star1.png"/>
        <img class="page6_header_star2_img" src="../assets/6/star2.png"/>
        <img class="page6_header_star3_img" src="../assets/6/star1.png"/>
        <img class="page6_header_star4_img" src="../assets/6/star1.png"/>
        <img class="page6_header_star_tranlate_img" src="../assets/6/star1.png"/>
      </header>
    </mt-swipe-item>

    <mt-swipe-item class="page7 item">
      <header style="width: 100%; height: 30%; position:relative;">
        <img class="page7_header_sun_img" src="../assets/7/sun.png"/>
        <img style="height: 60%; width: 130%; position: absolute;left: 0; bottom: 0; z-index: 1" class="page7_header_mountain_1_img" src="../assets/7/mountain1.png"/>
        <img style="height: 60%; width: 120%; position: absolute;left: 0; bottom: 0; z-index: 2" class="page7_header_mountain_2_img" src="../assets/7/mountain2.png"/>
        <img style="height: 60%; width: 150%; position: absolute;right: 0; bottom: 0; z-index: 2" class="page7_header_mountain_3_img" src="../assets/7/mountain3.png"/>
        <img style="position: absolute;left: 30%; bottom: 0; z-index: 3; width: 65%" class="page7_header_grassland_img" src="../assets/7/grassland.png"/>
        <img style="position: absolute;left: 20%;  bottom: 0; z-index: 4; width: 60%;" class="page7_header_train_img" src="../assets/7/train.png"/>

      </header>
      <div></div>
      <footer>

      </footer>
    </mt-swipe-item>
    <mt-swipe-item class="swip-item-3 item">
      <header style="height: 25%">
        <img style="width: 100%" src="../assets/4/header.png"/>
      </header>
      <div style="height: 30%">
        <div class="page4_content_title">2017年</div>
        <div class="page4_content_title">空中飞行了<b style="color: red">19999</b>千米</div>
        <div class="page4_content_title">相当于环绕地球<b style="color: red">3</b>圈</div>
      </div>
      <footer style="height: 45%" class="page4_footer">
          <img class="page4_earth_img" src="../assets/4/earth.png"/>
          <img class="page4_bg_line_img" src="../assets/4/line.png"/>
      </footer>
    </mt-swipe-item>
  </mt-swipe>
</template>

<script>
import { Swipe, SwipeItem  } from 'mint-ui';
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    'mt-swipe': Swipe,
    'mt-swipe-item': SwipeItem
  },
  created() {
  }
}
</script>

<style type="scss">
  .page6 {
    overflow-x: hidden;
  }
  .page7{
    overflow-x: hidden;
  }
  .item{
    text-align: center;
    font-size: 1rem;
    color: black;
  }
  /**
   *  第四页
   *  地球旋转
   *  add by yixuanz 2018-1-21 19:35:35
   */
  .page4_footer_content{
    position: absolute;
  }
  .page4_footer{
    position: absolute;
  }
  .page4_bg_line_img{
    z-index: 999;
    width: 13rem;
    position: relative;
    top: -7rem;
  }
  .page4_earth_img{
    -webkit-transition-property: -webkit-transform;
    -webkit-transition-duration: 1s;
    -moz-transition-property: -moz-transform;
    -moz-transition-duration: 1s;
    -webkit-animation: rotate 3s linear infinite;
    -moz-animation: rotate 3s linear infinite;
    -o-animation: rotate 3s linear infinite;
    animation: rotate 3s linear infinite;

    z-index: 1;
    width: 10rem;
    height: 10rem;
    position: relative;
  }
  @-webkit-keyframes rotate{from{-webkit-transform: rotate(0deg)}
    to{-webkit-transform: rotate(360deg)}
  }
  @-moz-keyframes rotate{from{-moz-transform: rotate(0deg)}
    to{-moz-transform: rotate(359deg)}
  }
  @-o-keyframes rotate{from{-o-transform: rotate(0deg)}
    to{-o-transform: rotate(359deg)}
  }
  @keyframes rotate{from{transform: rotate(0deg)}
    to{transform: rotate(359deg)}
  }
  /***
  * 月亮 第6页
  * add by yixuanz 2018-1-21 20:35:15
 */
  .page6_header{
    width: 100%;
    height: 50%;
    position: relative;
  }

  .page6_header_moon_img{
    -webkit-animation: moonTranslate 2s linear infinite alternate;
    -moz-animation: moonTranslate 2s linear infinite alternate;
    -o-animation: moonTranslate 2s linear infinite alternate;
    animation: moonTranslate 2s linear infinite alternate;

    width: 10rem;
    position: absolute;
    left: 22%;
    bottom: 3rem;
  }
  @-webkit-keyframes moonTranslate{
    from{transform: rotate(-15deg) }
    to{transform: rotate(15deg) }
  }

  .page6_header_star_tranlate_img{
    width: 1.7rem;

    position: absolute;
    right: 1rem;
    top: .2rem;
    -webkit-animation: starUpToDown 2s ease infinite 4s;
    -moz-animation: starUpToDown 2s ease infinite 4s;
    -o-animation: starUpToDown 2s ease infinite 4s;
    animation: starUpToDown 2s ease infinite 4s;
  }

  .page6_header_star1_img{
    width: 2.2rem;

    position: absolute;
    left: 3rem;
    top: 3rem;
    -webkit-animation: beat 2s linear infinite alternate;
    -moz-animation: beat 2s linear infinite alternate;
    -o-animation: beat 2s linear infinite alternate;
    animation: beat 2s linear infinite alternate;
  }

  .page6_header_star2_img{
    position: absolute;
    left: 3rem;
    bottom: 5rem;
    width: .8rem;

    -webkit-animation: beat 2s linear infinite alternate;
    -moz-animation: beat 2s linear infinite alternate;
    -o-animation: beat 2s linear infinite alternate;
    animation: beat 2s linear infinite alternate;
  }

  .page6_header_star3_img{
    position: absolute;
    right: 3rem;
    bottom: 3rem;
    width: .8rem;
    -webkit-animation: beat 2s linear infinite alternate;
    -moz-animation: beat 2s linear infinite alternate;
    -o-animation: beat 2s linear infinite alternate;
    animation: beat 2s linear infinite alternate;
  }

  .page6_header_star4_img{
    position: absolute;
    left: 4rem;
    bottom: 1rem;
    width: 1.5rem;

    -webkit-animation: beat 2s linear infinite;
    -moz-animation: beat 2s linear infinite;
    -o-animation: beat 2s linear infinite;
    animation: beat 2s linear infinite;
  }

  @keyframes beat {
    0% {-webkit-transform: scale(1)}
    15% {-webkit-transform: scale(1.2)}
    30% {-webkit-transform: scale(1)}
    55% {-webkit-transform: scale(1.1)}
    100% {-webkit-transform: scale(1)}
  }
  @-webkit-keyframes beat {
    0% {-webkit-transform: scale(1)}
    15% {-webkit-transform: scale(1.2)}
    30% {-webkit-transform: scale(1)}
    55% {-webkit-transform: scale(1.1)}
    100% {-webkit-transform: scale(1)}
  }

  @-webkit-keyframes starUpToDown {
    from{
      right: 1rem;
      top: .1rem;
      opacity: 1;
    }
    to{
      right: 100%;
      top: 15rem;
      opacity: 0;
    }
  }
  /***
  * 火车 第7页
  * add by yixuanz 2018-1-21 20:35:15
   */
  .page7_header_sun{
    width: 100%;
    height: 30%;
  }
  .page7_header_mountain_1_img{
    -webkit-animation: mountainTranslateLeft 5s linear infinite;
    -moz-animation: mountainTranslateLeft 5s linear infinite;
    -o-animation: mountainTranslateLeft 5s linear infinite;
    animation: mountainTranslateLeft 5s linear infinite;
  }
  .page7_header_mountain_2_img{
    -webkit-animation: mountainTranslateLeft 3s linear infinite;
    -moz-animation: mountainTranslateLeft 3s linear infinite;
    -o-animation: mountainTranslateLeft 3s linear infinite;
    animation: mountainTranslateLeft 3s linear infinite;
  }
  .page7_header_mountain_3_img{
    -webkit-animation: mountainTranslateLeft 3s linear infinite;
    -moz-animation: mountainTranslateLeft 3s linear infinite;
    -o-animation: mountainTranslateLeft 3s linear infinite;
    animation: mountainTranslateLeft 3s linear infinite;
  }

  @-webkit-keyframes mountainTranslateLeft{
    from{transform: translateX(15rem) }
    to{transform: translateX(0) }
  }

  .page7_header_sun_img {
    width: 3rem;
    position: absolute;
    right: 1.5rem;
    top: .5rem;

    -webkit-transition-property: -webkit-transform;
    -webkit-transition-duration: 1s;
    -moz-transition-property: -moz-transform;
    -moz-transition-duration: 1s;
    -webkit-animation: sunTranslateLeft 3s linear infinite;
    -moz-animation: sunTranslateLeft 3s linear infinite;
    -o-animation: sunTranslateLeft 3s linear infinite;
    animation: sunTranslateLeft 3s linear infinite;
  }
  @-webkit-keyframes sunTranslateLeft{
    from{transform: rotate(0deg); right: 0rem; top: 0 }
    to{transform: rotate(359deg); right: 70%; top:20%; }
  }
  @-moz-keyframes sunTranslateLeft{
    from{transform: rotate(0deg); right: 0rem; top: 0 }
    to{transform: rotate(359deg); right: 70%; top:20%; }
  }
  @-o-keyframes sunTranslateLeft{
    from{transform: rotate(0deg); right: 0rem; top: 0 }
    to{transform: rotate(359deg); right: 70%; top:20%; }
  }
  @keyframes sunTranslateLeft{
    from{transform: rotate(0deg); right: 0rem; top: 0 }
    to{transform: rotate(359deg); right: 70%; top:20%; }
  }
</style>
