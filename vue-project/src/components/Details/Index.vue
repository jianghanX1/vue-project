<template>
  <div class="details">
    <div class="main-center">
      <div class="main-game">
        <div class="game-part">
          <div class="game-container" :style="full">
            <iframe src="https://download-cdn21.vigoo.com/dinosaursniping-download/index.html" width="100%" height="100%"></iframe>
            <div class="close" :style="closeStyle" @click="closeClick"><i class="el-icon-close" /></div>
          </div>
          <div class="game-bar">
            <div class="bar-app-icon"><img :src="img2" alt=""></div>
            <div class="bar-btns">
              <div class="download"><span>Add to Desktop</span></div>
              <div class="play-tag"><span>Play MOTO Games</span></div>
              <div class="full-btn" @click="amplifyClick"><i class="el-icon-rank"></i></div>
            </div>
          </div>
        </div>
        <div class="game-rec">
          <div class="app-item"><img :src="img2" alt=""></div>
          <div class="app-item"><img :src="img3" alt=""></div>
          <div class="app-item"><img :src="img4" alt=""></div>
          <div class="app-item"><img :src="img5" alt=""></div>
          <div class="app-item"><img :src="img6" alt=""></div>
        </div>
      </div>
      <div class="main-waterfall">
        <div class="recommend-banner">
          <div class="app-item"><img :src="img2" alt=""></div>
          <div class="app-item"><img :src="img3" alt=""></div>
          <div class="app-item"><img :src="img4" alt=""></div>
          <div class="app-item"><img :src="img5" alt=""></div>
          <div class="app-item"><img :src="img6" alt=""></div>
          <div class="app-item"><img :src="img6" alt=""></div>
          <div class="app-item"><img :src="img6" alt=""></div>
          <div class="app-item"><img :src="img6" alt=""></div>
        </div>
        <div class="game-list">
          <div class="app-item" v-for="(item,index) in gameList" :key="index"><img :src="img2" alt=""></div>
          <div class="more-btn">
            <div>Load More Games</div>
          </div>
        </div>
      </div>
      <Bottom titleType="1" />
    </div>
    <div class="main-float">
      <div class="float-ads">

      </div>
      <div class="float-games">
        <div class="games-container">
          <div class="title">Top Games</div>
          <div class="game-warp">
            <div class="game-list">
              <div class="app-item"><img :src="img2" alt=""></div>
              <div class="app-item"><img :src="img3" alt=""></div>
              <div class="app-item"><img :src="img4" alt=""></div>
              <div class="app-item"><img :src="img5" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
            </div>
          </div>
        </div>
        <div class="games-container">
          <div class="title">New Games</div>
          <div class="game-warp">
            <div class="game-list">
              <div class="app-item"><img :src="img2" alt=""></div>
              <div class="app-item"><img :src="img3" alt=""></div>
              <div class="app-item"><img :src="img4" alt=""></div>
              <div class="app-item"><img :src="img5" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
            </div>
          </div>
        </div>
        <div class="games-container" id="girlsGames">
          <div class="title">Girls Games</div>
          <div class="game-warp">
            <div class="game-list">
              <div class="app-item"><img :src="img2" alt=""></div>
              <div class="app-item"><img :src="img3" alt=""></div>
              <div class="app-item"><img :src="img4" alt=""></div>
              <div class="app-item"><img :src="img5" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
              <div class="app-item"><img :src="img6" alt=""></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import img2 from '@/assets/02.webp'
import img3 from '@/assets/03.webp'
import img4 from '@/assets/04.webp'
import img5 from '@/assets/05.webp'
import img6 from '@/assets/06.webp'
import Bottom from '@/components/HomeIndex/Bottom';

export default {
  name: "Index",
  components: {
    Bottom
  },
  data() {
    return {
      img2, img3, img4, img5, img6,
      gameList: [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],
      full: null,
      fullStyle: {
        position: "fixed",
        width: "100%",
        height: "100%",
        left: 0,
        top: 0,
        zIndex: 999
      },
      closeStyle: null,
    }
  },
  methods: {
    amplifyClick() {
      this.full = this.fullStyle
      this.closeStyle = {
        display: 'block',
        position: "absolute",
        right: "12px",
        top: "10px",
        zIndex: 50,
        fontSize: "32px",
        color: '#ffffff',
        cursor: 'pointer'
      }
    },
    closeClick() {
      this.full = null
      this.closeStyle = null
    }
  },
  mounted() {
    let headdiv=document.getElementById("girlsGames");
    let nTop = headdiv.offsetTop;
    window.onscroll = function () {
      //??????scrollTop?????????????????????????????????????????????
      let scrollTop = document.documentElement.scrollTop||document.body.scrollTop;
      console.log(scrollTop);

      console.log(nTop);
      if (scrollTop > nTop) {
        headdiv.style.position = "fixed"
        headdiv.style.top = "10px"
      } else {
        headdiv.style.position="relative";
      }
    }
  }
}
</script>

<style lang="less" scoped>
@media screen and (min-width: 1883px){
  .details {
    width: 1875px;
    position: relative;
    .main-center {
      margin-left: 520px;
      box-sizing: border-box;
    }
    .float-games .games-container {
      width: 520px;
    }
  }
  .float-games .games-container .game-list .app-item {
    margin-right: 6px;
  }
  .float-games .games-container .game-list .app-item:nth-child(4n) {
    margin-right: 0;
  }
}
@media screen and (min-width: 1755px) and (max-width: 1882px){
  .details{
    width: 1747px;
    position: relative;
  }
  .main-center {
    margin-left: 392px;
    box-sizing: border-box;
  }
  .float-games .games-container {
    width: 392px;
  }
}
@media screen and (min-width: 1627px) and (max-width: 1754px){
  .details{
    width: 1619px;
    position: relative;
    .main-center {
      margin-left: 264px;
      box-sizing: border-box;
    }
  }
  .float-games .games-container {
    width: 264px;
  }
}
@media screen and (min-width: 1499px) and (max-width: 1626px){
  .details{
    width: 1491px;
    position: relative;
    .main-center {
      margin-left: 136px;
      box-sizing: border-box;
    }
  }
  .float-games .games-container {
    width: 136px;
  }
}
@media screen and (max-width: 1498px){
  .float-games {
    display: none;
  }
}
@media screen and (min-width: 1363px) and (max-width: 1498px){
  .details{
    width: 1355px;
    position: relative;
  }
}
@media screen and (min-width: 1263px) and (max-width: 1362px){
  .details{
    width: 1255px;
    position: relative;
    .main-center {
      width: 955px;
      padding: 0 18px 0 5px;
      box-sizing: border-box;
      .recommend-banner .app-item:nth-of-type(1){
        display: none;
      }
      .game-list .app-item {
        float: left;
        margin-right: 13px;
      }
      .game-list .app-item:nth-child(7n) {
        margin-right: 0;
      }
    }
  }
}
@media screen and (min-width: 1363px){
  .main-center {
    width: 1055px;
    padding: 0 18px 0 5px;
    box-sizing: border-box;
  }
  .main-game .game-container {
    width: 900px;
    height: 570px;
    overflow: hidden;
    position: relative;
  }
  .main-waterfall .game-list .app-item {
    float: left;
    margin-right: 8px;
  }
  .main-waterfall .game-list .app-item:nth-child(8n) {
    margin-right: 0;
  }
}
@media screen and (max-width: 1362px){
  .main-game .game-container {
    width: 800px;
    height: 570px;
    overflow: hidden;
    position: relative;
  }
  .main-waterfall .game-list .app-item {
    float: left;
    margin-right: 8px;
  }
}
@media screen and (min-width: 1263px){
  .float-ads {
    display: block;
  }
}
@media screen and (max-width: 1262px){
  .main-center {
    width: 955px;
    padding: 0 18px 0 5px;
    margin: 0 auto;
    box-sizing: border-box;
  }
  .recommend-banner .app-item:nth-of-type(1){
    display: none!important;
  }
  .main-waterfall .game-list .app-item {
    float: left;
    margin-right: 13px;
  }
  .main-waterfall .game-list .app-item:nth-child(7n) {
    margin-right: 0;
  }
}
.details{
  margin: 10px auto 0;
  position: relative;
  .main-game {
    margin-bottom: 13px;
    height: 632px;
    .game-part {
      float: left;
      .game-container {
        .close{
          display: none;
        }
      }
      .game-bar{
        height: 60px;
        background-color: rgba(0,0,0,.3);
        padding-left: 6px;
        display: flex;
        justify-content: space-between;
        .bar-app-icon {
          width: 48px;
          height: 48px;
          border-radius: 8px;
          overflow: hidden;
          margin-top: 6px;
          img{
            width: 100%;
            height: 100%;
          }
        }
        .bar-btns{
          margin-right: 10px;
          display: flex;
          .download {
            height: 40px;
            background-color: #3be6a2;
            border-radius: 8px;
            margin-top: 10px;
            margin-left: 12px;
            padding: 0 10px 0 8px;
            cursor: pointer;
            span{
              line-height: 40px;
              font-size: 16px;
              color: #fff;
            }
          }
          .play-tag{
            height: 40px;
            line-height: 40px;
            text-align: center;
            padding: 0 12px;
            margin-top: 10px;
            border-radius: 8px;
            background-color: hsla(0,0%,100%,.2);
            margin-left: 12px;
            font-size: 13px;
            color: #fff;
          }
          .full-btn{
            width: 30px;
            height: 30px;
            display: block;
            background-color: transparent;
            margin-top: 15px;
            float: left;
            margin-left: 8px;
            position: relative;
            transform: rotate(45deg);
            /deep/ .el-icon-rank{
              font-size: 36px;
              color: #ffffff;
            }
          }
        }
      }
    }
    .game-rec {
      float: left;
      margin-left: 18px;
      .app-item{
        margin-bottom: 15px;
        width: 114px;
        height: 114px;
        padding: 2px 4px 4px 2px;
        box-sizing: border-box;
        cursor: pointer;
        img{
          width: 100%;
          height: 100%;
          border-radius: 12px;
          border: 2px solid #fff;
        }
      }
    }
  }
  .main-waterfall {
    margin-bottom: 20px;
    .recommend-banner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
      height: 122px;
    }
    .game-list{
      min-height: 300px;
      .more-btn {
        clear: both;
        padding-top: 10px;
        div{
          cursor: pointer;
          margin: 24px auto 0;
          background-color: #f83123;
          border-radius: 8px;
          height: 56px;
          width: 500px;
          color: #fff;
          font-size: 22px;
          text-align: center;
          display: block;
          box-shadow: 0 6px 8px 0 rgb(0 0 0/20%);
          line-height: 56px;
        }
      }
    }
  }
  .main-desc{
    margin: 18px auto 0;
    background-color: rgba(0,0,0,.15);
    padding: 28px 26px;
    word-break: break-word;
    word-wrap: break-word;
    border-radius: 10px;
  }
  .main-float {
    .float-games {
      position: absolute;
      left: 0;
      top: 0;
      .games-container{
        .title{
          height: 40px;
          line-height: 40px;
          text-align: center;
          font-size: 20px;
          color: #fff;
          background-color: #f83123;
        }
        .game-warp {
          padding: 2px 0 6px;
          background-color: rgba(0,0,0,.3);
          .game-list {
            padding: 6px 7px 0;
            height: 390px;
            overflow: hidden;
            .app-item {
              margin-bottom: 6px;
              float: left;
            }
          }
        }
      }
    }
  }
  .app-item {
    width: 122px;
    height: 122px;
    display: block;
    overflow: hidden;
    margin-bottom: 10px;
    position: relative;
    padding: 2px 4px 4px 2px;
    box-sizing: border-box;
    cursor: pointer;
    img{
      width: 100%;
      height: 100%;
      border: 2px solid #fff;
      border-radius: 12px;
    }
  }
  @keyframes example {
    0%  {transform: scale(1);}
    35%  {transform: scale(1.05);}
    65% {transform: scale(1.03);}
    100% {transform: scale(1.08);}
  }
  .app-item:hover{
    cursor: pointer;
    animation-name: example;
    animation-duration: 0.6s;
    animation-timing-function: linear;
    animation-delay: 0s;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: forwards;
    animation-play-state: running;
    z-index: 1;
  }
}
</style>
