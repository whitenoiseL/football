<template>
  <div class='content'>
    <div class="battle-box">
      <div class="line left">
        <div class="item">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
        <div class="item">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
      </div>
      <div class="line left">
        <div class="item">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
        <div class="item">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
      </div>
      <div class="line">
        <div class="item">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
        <i class="mid-icon fa fa-futbol-o" aria-hidden="true"></i>
        <div class="item me">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
      </div>
      <div class="line right">
        <div class="item me">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
        <div class="item me">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
      </div>
      <div class="line right">
        <div class="item me">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
        <div class="item me">
          <div class='player-box'>
            <player></player>
          </div>
        </div>
      </div>
    </div>
    <div class="live-box">
      <div class="text-live">

      </div>
      <el-button class='skip-btn'>跳过</el-button>
    </div>
    <!-- <ul class='defense-list'>
      <li v-for='item in defenseList' :key='item'>
        <div class="defense-players">
          <defense-list></defense-list>
        </div>
      </li>
    </ul> -->
  </div>
</template>

<script>
import player from "../components/miniPlayer";

export default {
  components: {
    player
  },
  data() {
    return {
      defenseList: [1, 2]
    };
  },
  computed: {},
  methods: {}
};
</script>

<style lang='scss' scoped>
.content {
  display: flex;
  align-items: flex-start;
  background-color: rgba(0, 0, 0, 0.5);
  padding: 20px;
  .battle-box {
    width: 50%;
    display: flex;
    flex-direction: column;
    padding: 20px;
    height: 100%;
    .line {
      display: flex;
      width: 100%;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 20px;
      &.left {
        justify-content: flex-start;
      }
      &.right {
        justify-content: flex-end;
      }
    }
    .item {
      display: flex;
      justify-content: center;
      text-align: center;
      margin-right: 40px;
      background-color: rgba(233, 23, 32, 0.7);
      border-radius: 10px;
      position: relative;
      overflow: hidden;
      &.me {
        background-color: rgba(255, 215, 3, 0.7);
      }
      .player-box {
      }
    }
  }
  .live-box {
    width: 50%;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    .text-live {
      width: 100%;
      height: 700px;
      background-color: rgba(255, 255, 255, 0.5);
    }
    .skip-btn {
      width: 80%;
      margin-top: 40px;
      color: #fff;
      font-size: 20px;
      background-color: #3cac54;
      border-color: #3cac54;
      border-radius: 60px;
    }
  }
}
.mid-icon {
  font-size: 100px;
  color: #aaa;
}
</style>
