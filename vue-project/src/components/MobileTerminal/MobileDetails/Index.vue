<template>
  <div class="mobile-details">
    <div class="nav-bar">
      <div>VIGOO GAMES</div>
    </div>
    <div class="details-top-box">
      <div class="app-base">
        <div class="app-pic"><img :src="img6" alt=""></div>
        <div class="app-info">
          <p class="app-name">Stickman Hook Rescue</p>
          <div class="app-btns">
            <div class="app-collection"></div>
          </div>
        </div>
      </div>
      <button class="app-play">
        11111
        <div class="play-fill"></div>
      </button>
    </div>
  </div>
</template>

<script>
import img6 from '@/assets/06.webp'
export default {
  name: "Index",
  data() {
    return {
      img6
    }
  }
}
</script>

<style lang="less" scoped>
.mobile-details{
  .nav-bar{
    height: 2.8125rem;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    box-shadow: 0 0.125rem 0.1875rem 0 rgba(0,16,63,.4);
    background-color: #f83123;
    z-index: 1;
    div{
      font-size: 1.125rem;
      text-align: center;
      line-height: 2.8125rem;
      color: #ffffff;
      font-weight: bold;
    }
  }
  .details-top-box{
    margin-top: 3.5625rem;
    .app-base:after{
      content: ".";
      display: block;
      height: 0;
      clear: both;
      visibility: hidden;
    }
    .app-pic{
      margin-left: 0.625rem;
      border: 2px solid #fff;
      border-radius: 0.625rem;
      overflow: hidden;
      width: 4.75rem;
      height: 4.75rem;
      float: left;
      background-color: #fff;
      img{
        width: 100%;
        height: 100%;
      }
    }
    .app-info{
      padding-top: 0.5rem;
      float: left;
      margin-left: 0.9375rem;
      .app-name{
        color: #fff;
        font-size: 1rem;
        font-weight: 700;
      }
      .app-btns{
        margin-top: 0.6875rem;
        .app-collection{
          float: left;
          width: 1.625rem;
          height: 1.625rem;
          border-radius: 0.3125rem;
          background-color: #f09;
          position: relative;
          border: 0.125rem solid #fff;
        }
      }
      .app-btns:after{
        content: ".";
        display: block;
        height: 0;
        clear: both;
        visibility: hidden;
      }
    }
    .app-play{
      margin: 0.6rem auto 0;
      width: 18.75rem;
      border-radius: 0.625rem;
      border: 0.125rem solid #fff;
      height: 2.625rem;
      position: relative;
      display: block;
      overflow: hidden;
      background-color: #ccc;
      .play-fill{
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        width: 100%;
        background-color: #f09;
        max-width: 100%;
        transition: width .5s linear;
        z-index: 1;
      }
    }
    .app-play:before {
      content: "Play Now";
      font-size: .9375rem;
      position: absolute;
      top: 50%;
      transform: translate(-50%, -50%);
      left: 50%;
      color: #fff;
      z-index: 2;
    }
    .app-play:after{
      content: "";
      border-color: transparent transparent transparent #fff;
      border-style: solid;
      border-width: 0.58125rem 1.04rem;
      width: 0;
      height: 0;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      left: 3rem;
      animation-duration: 0.3s;
      animation-timing-function: ease;
      animation-delay: 0s;
      animation-iteration-count: infinite;
      animation-direction: normal;
      animation-fill-mode: none;
      animation-play-state: running;
      animation-name: playAmt;
      z-index: 3;
    }
    @keyframes playAmt {
      0%  {left: 3rem;}
      35% {left: 3.3rem;}
      65% {left: 3.8rem;}
      100% {left: 4rem;}
    }
  }
}
</style>
