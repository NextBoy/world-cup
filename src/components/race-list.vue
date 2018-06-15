<template>
  <div>
    <header>
      <img src="../images/hd.png" alt="">
      <h1>精彩赛事</h1>
    </header>
    <div class="card-item-wrap">
      <div class="date">2017-1-12 <span>23:00</span></div>
      <div class="card-item">
        <div class="left box">
          <img src="http://placehold.it/50x35" class="flag">
          <p>中国</p>
        </div>
        <div class="not-start center box">
          <p>预约提醒</p>
          <p>VS</p>
        </div>
        <div class="right box">
          <img src="http://placehold.it/50x35" class="flag">
          <p>中国</p>
        </div>
      </div>
    </div>
    <div class="card-item-wrap">
      <div class="date">2017-1-12 <span>23:00</span></div>
      <div class="card-item">
        <div class="left box">
          <img src="http://placehold.it/50x35" class="flag">
          <p>中国</p>
        </div>
        <div class="over center box">5 - 6</div>
        <div class="right box">
          <img src="http://placehold.it/50x35" class="flag">
          <p>中国</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'race-list',
    props: ['list']
  }
</script>
<style lang="less" scoped>
  header {
    text-align: center;
    img {
      width: 90vw;
      height: 130px;
      border-radius: 5px;
      margin: 10px auto;
    }
    padding-bottom: 15px;
  }
  .card-item-wrap {
    .date {
      text-align: center;
      color: deepskyblue;
      span {
        color: red;
        font-weight: bold;
      }
    }
  }
  .card-item {
    margin: 0 auto;
    width: 85vw;
    height: 70px;
    padding: 10px 6px;
    margin-bottom: 10px;
    background: white;
    box-shadow: 0 4px 16px 0 rgba(18, 21, 58, 0.14);
    border-radius: 6px;
    display: flex;
    flex-direction: row;
    .box {
      height: 70px;
      flex: 1;
      text-align: center;
    }
    .left {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      p {
        line-height: 1.5;
      }
    }
    .right {
      .left;
    }
    .center {
      width: 50%;
      border-radius: 5px;
      .left;
    }
    .not-start {
      background: dodgerblue;
      color: white;
    }
    .over {
      color: white;
      background: gray;
      font-size: 25px;
      font-weight: bold;
    }
    .flag {
      width: 50px;
      height: 35px;
    }
  }
</style>
