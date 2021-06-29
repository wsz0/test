<template>
	<view class="container">
		
  <view class="uni-flex uni-row">
                <view class="box" style="background-color: #007AFF;">A</view>
                <view class="box" style="background-color: #4CD964;">B</view>
                <view class="box" style="background-color: #F0AD4E;">C</view>
            </view>
		<uni-link :href="href" :text="href"></uni-link>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
			}
		},
		methods: {

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
