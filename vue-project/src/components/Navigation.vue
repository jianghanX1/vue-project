<template>
    <div>
      <div class="bj">
        <div class="title">ViGOO GAMES</div>
        <div class="nav-list">
          <div>New Games</div>
          <div>Girl Games</div>
          <div>MMORPG</div>
          <div>Top Games</div>
          <div>New Games</div>
          <div>New Games</div>
          <div>New Games</div>
        </div>
        <div class="search">
          <el-input
            placeholder="Search Games"
            prefix-icon="el-icon-search"
            v-model="searchInput">
          </el-input>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Banner',
  data () {
    return {
      searchInput: null
    }
  },
  created() {
    if (/Mobi|Android|iPhone/i.test(navigator.userAgent)) {
      console.log(111)

    } else {
      console.log(2)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
  .bj{
    height: 56px;
    background: #f83123;
    color: #ffffff;
    display: flex;
    justify-content: space-between;
    .title{
      min-width: 200px;
      line-height: 56px;
      font-size: 18px;
      font-weight: bold;
      margin-left: 36px;
      cursor: pointer;
    }
    .nav-list{
      overflow: hidden;
      line-height: 56px;
      div{
        float: left;
        margin-left: 15px;
      }
      div:hover{
        background-color: rgba(0,0,0,.1);
        border-top: 4px solid #fff81a;
        cursor: pointer;
      }
    }
  }
  .search{
    margin-right: 15px;
  }
  /deep/ .el-input {
    width: 327px;
    margin-top: 7px;
  }
  /deep/ .el-input--prefix .el-input__inner{
    background: rgba(0,0,0,.3);
    border: 0;
    color: #f4d0ce;
    font-size: 16px;
  }
  /deep/ .el-input--prefix .el-input__inner:focus{
    background: #ffffff;
    border: 0;
    color: #333;
    font-size: 16px;
  }
</style>
