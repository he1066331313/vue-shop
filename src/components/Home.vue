<template>
	<div id="home">
		<div class="nav">
			<ul>
				<li v-for="(item,key) in navList" @mouseover="navShow(key)"  v-bind:class="{actived:isActive==key}">
					{{item}}
				</li>
			</ul>
			<div class="logo">
				<img src="../assets/logo.png" alt="">
			</div>
			<div class="icon">
				<img src="../assets/search.png" alt="">
				<img src="../assets/user.png" alt="">
				<img src="../assets/buy.png" alt="">
			</div>
		</div>
		<div class="nav-bar">
			<ul>
				<li v-for="item in ladyList" v-if="lshow == 0">
					{{item}}
				</li>
				<li v-for="item in manList" v-if="mshow == 1">
					{{item}}
				</li>
				<li v-for="item in childList" v-if="cshow == 2">
					{{item}}
				</li>
			</ul>
		</div>
		<div class="banner">
			<img src="../assets/1.jpg" alt="">
		</div>
		<div class="banner1">
			<div class="b1-left">
				<img src="../assets/21.jpg" alt="">
				<p>法式內搭,最新到货</p>
			</div>
			<div class="b2-right">
				<img src="../assets/22.jpg" alt="">
				<p>经典系列底价回馈</p>
			</div>
		</div>
		<div class="footer">
			
		</div>
	</div>
</template>

<script>
	
	export default {
		data() {
			return {
				'isActive':0,
				'navList':['女士','男士','儿童'],
				'ladyList':['当季新品','服装','鞋靴','箱包','配件','品牌','特卖'],
				'manList':['当季新品','服装','鞋靴','箱包','配件','品牌','特卖1'],
				'childList':['当季新品','女童装','男童装','女童鞋','男童鞋','婴童装','婴童配饰','品牌','特卖'],
				'lshow':'',
				'mshow':'',
				'cshow':''
			};
		},
		methods:{
			navShow(key){
				this.isActive = key;
				this.lshow = key;
				this.mshow = key;
				this.cshow = key;	
			}
// 			navHidden(){
// 				this.isActive = 0;
// 				this.lshow = 0;
// 				this.mshow = '';
// 				this.cshow = '';
// 			}
		}
	}
</script>

<style scoped>
	div.nav .actived{
		color: #000;
	}
	div#home{
		width: 80%;
		margin: 0 auto;
		min-width: 1000px;
	}
	div.nav{
		width: 100%;
		height: 80px;
		display: flex;

	}
	div.nav ul{
		width: 20%;
		display: flex;
		list-style: none;
	}
	div.nav ul li{	
		width: 33%;
		text-align: center;
		line-height: 80px;
		font-weight: 900;
		font-size: large;
		color: #999;
		cursor: pointer;
	}
	div.logo{
		display: flex;
		align-items: center;
		width: 60%;
		justify-content:center;
	}
	div.logo img{
		transform: scale(0.2);
	}
	div.icon{
		width: 20%;
		display: flex;
		align-items: center;
	}
	div.icon img{
		/* transform:scale(0.2); */
		width: 12%;
		height: 20%;
		margin-left: 30px;
	}	
	div.nav-bar ul{
		width: 800px;
		margin: 0 auto;
		list-style: none;
		display: flex;
	}
	div.nav-bar ul li{
		width: 30%;
		font-size: 14px;
		font-weight: bold;
		text-align: center;
		height: 40px;
		line-height: 40px;
	}
	div.banner{
		width: 1200px;
		margin-top: 20px;
		height: 765px;
		overflow: hidden;
	}
	div.banner img{
		width: 100%;
		height: 100%;
	}
	div.banner img:hover{
		transform: scale(1.1);
	}
	div.banner1{
		display: flex;
		width: 1200px;
		margin-top: 20px;	
	}
	div.banner1 div{
		width: 580px;
		height: 800px;
		overflow: hidden;
	}
	div.banner1 div p{
		text-align: center;
	}
	div.banner1 img{
		width: 100%;
		height: 90%;
	}
	div.banner1 img:hover{
		transform: scaleX(1.1);
	}
	div.b2-right{
		margin-left: 40px;
	}
	.footer{
		height: 600px;
	}
</style>
