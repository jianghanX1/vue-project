<template>
  <div>
    <div class="mobile-details" :style="playValue ? {display: 'none'} : {display: 'block'}">
      <div class="nav-bar">
        <div>VIGOO GAMES</div>
      </div>
      <div class="details-top-box">
        <div class="app-base">
          <div class="app-pic"><img :src="img6" alt=""></div>
          <div class="app-info">
            <p class="app-name">Stickman Hook Rescue</p>
            <div class="app-btns">
              <div class="app-collection">

              </div>
            </div>
          </div>
        </div>
        <button class="app-play" @click="playClick">
          <div class="play-fill"></div>
        </button>
      </div>
      <div class="details-seo-box">
        <div class="seo-tags">
          <a class="seo-tag" style="color: #f5b417">Obstacle Games</a>
          <a class="seo-tag" style="color: #54abd7">Adventure Games</a>
          <a class="seo-tag" style="color: #ff6215">Action Games</a>
        </div>
      </div>
      <div class="details-recommend-box">
        <p class="recommend-title">Recommendations for similar games</p>
        <div class="recommend-list">
          <ClassList styleType="1"></ClassList>
        </div>
      </div>
    </div>
    <div class="app-module" :style="playValue ? {display: 'block'} : {display: 'none'}">
      <div class="app-iframe">
        <div class="iframe-box">
          <iframe id="gameIframe" src="https://download.vigoogames.com/sogame-download/ShortcutPro/index.html" width="100%" height="100%"></iframe>
        </div>
        <div class="iframe-back" @click="backClick"><i class="el-icon-arrow-left"></i></div>
      </div>
      <div class="app-promote">
        <div class="promote-list">
          <div class="item" @click="detailsClick"><img :src="img6" alt=""></div>
          <div class="item"><img :src="img6" alt=""></div>
          <div class="item"><img :src="img6" alt=""></div>
          <div class="item"><img :src="img6" alt=""></div>
          <div class="item"><img :src="img6" alt=""></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import img6 from '@/assets/06.webp';
import ClassList from "@/components/MobileTerminal/MobileHome/ClassList";
export default {
  name: "Index",
  components: {
    ClassList
  },
  data() {
    return {
      img6,
      playValue: false
    }
  },
  methods: {
    playClick() {
      this.playValue = true
    },
    backClick() {
      this.playValue = false
    },
    detailsClick() {
      this.$router.push({
        path: '/mobileDetails'
      },()=>{})
      this.playValue = false
    }
  }
}
</script>

<style lang="less" scoped>
.mobile-details{
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  overflow: auto;
  z-index: 3;
  background-color: #0054ff;
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
  .details-seo-box{
    box-sizing: border-box;
    margin: 0.7rem auto 0;
    width: 18.75rem;
    border-radius: 0.3125rem;
    background-color: rgba(0,0,0,.2);
    max-height: 9.375rem;
    overflow: auto;
    padding: 0 0.625rem;
    .seo-tags {
      padding-top: 0.625rem;
      .seo-tag{
        float: left;
        margin-right: 0.5rem;
        padding: 0.3rem 0.4375rem;
        font-size: .625rem;
        color: #fff;
        border-radius: 0.125rem;
        margin-bottom: 0.5rem;
        line-height: 1;
        background-color: #fff;
      }
    }
    .seo-tags:after{
      content: ".";
      display: block;
      height: 0;
      clear: both;
      visibility: hidden;
    }
  }
  .details-recommend-box{
    margin-top: 0.875rem;
    padding: 0 0.625rem;
    .recommend-title{
      color: #fff;
      font-size: .9375rem;
    }
    .recommend-list{
      margin-top: 0.625rem;
    }
  }
}
.app-module {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: 2;
  background-color: #0b2167;
  overflow: hidden;
  .app-iframe{
    width: 100%;
    height: calc(100vh - 4.375rem);
    .iframe-box{
      width: 100%;
      height: 100%;
    }
  }
}
@media screen and (orientation: portrait){
  .app-iframe {
    max-width: 100%;
    max-height: 100%;
    margin: 0 auto;
    position: relative;
    .iframe-back{
      position: absolute;
      left: 0;
      top: 1.125rem;
      box-shadow: 0 0.125rem 0 0.0625rem rgb(52 126 223);
      border-radius: 0 1.125rem 1.125rem 0;
      overflow: hidden;
      width: 3.375rem;
      height: 2.1875rem;
      background-color: #589df7;
      text-align: center;
      /deep/ .el-icon-arrow-left{
        font-size: 2rem;
        color: #ffffff;
        line-height: 2.1875rem;
      }
    }
  }
  .app-promote {
    height: 4.375rem;
    overflow: hidden;
    background-color: #0073dd;
    padding: 0.5rem 0;
  }
  .app-promote .promote-list {
    white-space: nowrap;
    overflow: hidden;
    font-size: 0;
  }
  .app-promote .promote-list .item{
    display: inline-block;
    width: 3.5rem;
    height: 3.5rem;
    margin-left: 0.42rem;
    border-radius: 0.875rem;
    color: #333;
    overflow: hidden;
    background-color: #e4e4e4;
    img{
      width: 100%;
      height: 100%;
    }
  }
}
</style>
