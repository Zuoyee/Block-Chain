<template>
  <div class="card">
    <div class="logo">
			<img :src="info.img" alt="">
		</div>
		<div class="info">
			<h2>{{info.name}}</h2>
			<span>{{info.score}}</span>
		</div>
  </div>
</template>

<script>
  export default {
		name: 'card',
		props: ['info'],

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
  .card {
    display: flex;
    flex-direction: row;
		border: 1px solid #ccc;
		width: 250px;
		height: 100px;
		margin: 10px 0;
		border-radius: 10px;

		.logo {
			img {
				width: 50px;
				height: 50px;
				border-radius: 2px;
				margin: 10px;
			}
		}

		.info {
			flex: 1;

			h2 {
				font-weight: normal;
				font-size: 16px;
				margin-bottom: 10px;
			}

			span {
				background-color: red;
				color: #ffffff;
				padding: 2px;
				border-radius: 5px;
			}
		}
    
  }
</style>
