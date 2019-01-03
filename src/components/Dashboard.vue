<template>
  <div class="dashboard">
    <div class="head">
      <img src="../assets/1.png" alt="">
      <span class="logoName">超市BC积分</span>
    </div>
    <div class="main">
      <div class="banner">
        <div class="score">
          <img src="../assets/15.png" alt="">
        </div>
        <div class="user">
          <User></User>
        </div>
      </div>
      <div class="redeem">
        <h1>积分兑换</h1>
        <div>
          <Card v-for="(item, index) in redeem" :info="item"></Card>
        </div>
      </div>
      <div class="redeem">
        <h1>实物兑换</h1>
        <div>
          <Card v-for="(item, index) in exchange" :info="item"></Card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import User from './User';
  import Card from './Card';

  export default {
    name: 'dashboard',
    components: {
      User,
      Card
    },

    data() {
      return {
        redeem: [{
          img: 'static/2.png',
          name: '沃沃超市10元现金券',
          score: '100G'
        }, {
          img: 'static/3.png',
          name: '天天超市30元现金券',
          score: '300G'
        }, {
          img: 'static/4.png',
          name: '唯唯超市50元现金券',
          score: '500G'
        }, {
          img: 'static/5.png',
          name: '拼拼超市9.0折优惠券',
          score: '2000G'
        }, {
          img: 'static/6.png',
          name: '苏苏商城9.5折优惠券',
          score: '1800G'
        }, {
          img: 'static/7.png',
          name: '京京商城100元现金券',
          score: '1000G'
        }],
        exchange: [{
          img: 'static/9.png',
          name: '沃沃超市电冰箱',
          score: '8000G'
        }, {
          img: 'static/12.png',
          name: '天天超市充电宝',
          score: '600G'
        }, {
          img: 'static/10.png',
          name: '唯唯超市YSL口红',
          score: '3000G'
        }, {
          img: 'static/11.png',
          name: '拼拼超市电竞椅',
          score: '2000G'
        }, {
          img: 'static/13.png',
          name: '苏苏商城空调',
          score: '1800G'
        }, {
          img: 'static/14.png',
          name: '京京商城键盘',
          score: '1000G'
        }]
      }
    },
    
    beforeCreate: function() {
      
    },

    methods: {
      
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .dashboard {
    display: flex;
    flex-direction: column;

    .head {
      width: 100%;
      height: 80px;
      background-color: #000;
      display: flex;
      align-items: center;
      position: relative;

      img {
        height: 50px;
        position: absolute;
        left: 20%;
      }

      span {
        color: #ffffff;
        position: absolute;
        left: 24%;
      }
    }

    .main {
      flex: 1;
      padding: 20px 20%;

      .banner {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        overflow: hidden;
        height: 270px;

        .score {
          margin-right: 20px;
          height: 100%;
          width: 67%;

          img {
            width: 100%;
            height: 100%;
          }
        }

        .user {
          flex: 1;
        }
      }

      .redeem {
        h1 {
          border-left: 5px solid green;
          font-size: 24px;
          color: green;
          padding-left: 10px;
        }

        div {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          flex-wrap: wrap;
        }
      }
    }
  }
</style>
