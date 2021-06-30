<template>
	<view class="container">
		
  <view class="uni-flex uni-row">
				<button @click="get">aaa</button>
                <view class="box" style="background-color: #007AFF;">A</view>
                <view class="box" style="background-color: #4CD964;">B</view>
                <view class="box" style="background-color: #F0AD4E;" name="a">{{text1}}</view>
            </view>
			<view>
				<input type="" />
			</view>
		<uni-link :href="href" :text="href"></uni-link>
	</view>
</template>

<script>
	export default {
		data() {
			
			return {
				text1:'',
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
				,

			}
		},
		onLoad(){
			let that=this
					uni.request({
							url: 'http://localhost:52325/api/Aa/sendHello',
							method: 'GET',
							
							success(res){
								//console.log(res);
								//that.text1=res.data;
								//console.log(this);
								console.log(that);
								
							}
						});
			
		},
		methods: {
				get(){
					let that=this
					uni.request({
							url: 'http://localhost:52325/api/Aa/sendHello',
							method: 'GET',
							
							success(res){
								//console.log(res);
								that.text1=res.data;
								//console.log(this);
								console.log(that);
								
							}
						});
				}
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
	.box{
		width: auto;
		height: 100px;
	}
</style>
