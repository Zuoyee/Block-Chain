<template>
  <div class="user">
    <div class="avatar">
			<img src="../assets/8.png" alt="">
		</div>
		<div class="info">
			<div>
				<span>等级</span>
				<span class="grade">农民</span>
			</div>
			<div>
				<span>积分</span>
				<span class="score">1050G</span>
			</div>
		</div>
		<div class="button">
			<button>打卡赚取积分</button>
		</div>
  </div>
</template>

<script>
  export default {
    name: 'user',

    data() {
      return {
        
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
  .user {
    display: flex;
    flex-direction: column;
		border: 1px solid #ccc;
		height: 268px;
		align-items: center;
		justify-content: center;
    
		.avatar {
			flex: 3;
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: center;
			width: 100%;
			height: 120px;
			text-align: center;
			border-bottom: 1px solid #ccc;

			img {
				width: 100px;
				height: 100px;
				border-radius: 100px;
			}
		}
		
		.info {
			flex: 1;
			width: 100%;
			display: flex;
			flex-direction: row;
			justify-content: space-around;
			border-bottom: 1px solid #ccc;

			div {
				margin: 15px;

				span {
					border: 1px solid #ccc;
					padding: 3px;
				}

				span.grade {
					background-color: #000;
					color: #ffffff;
				}

				span.score {
					background-color: red;
					color: #ffffff;
				}
			}
		}

		.button {
			width: 100%;
			flex: 1;
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: center;

			button {
				width: 80%;
				height: 30px;
			}
		}
  }
</style>
