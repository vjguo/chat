<template>
	<view class="top-bar">
		<view class="top-bar__left">
			<slot name="left"></slot>
		</view>
		<view class="top-bar__center">
			<slot name="center"></slot>
		</view>
		<view class="top-bar__right">
			<slot name="right"></slot>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.top-bar {
		z-index: 100;
		position: fixed;
		top:0;
		left:0;
		display: flex;
		align-items: center;
		height:88rpx;
		width: 100%;
		box-sizing: border-box;
		box-shadow: 0px 1px 0px 0px rgba(0,0,0,.1);
		// 解决手机顶部状态栏内容被覆盖
		// padding-top: var(--status-bar-height);
		
		.top-bar__left {
			display: flex;
			align-items: center;
			float: left;
			padding-left: $uni-spacing-row-base;
		}
		
		.top-bar__center {
			flex: 1;
			text-align: center;
		}
		
		.top-bar__right {
			display: flex;
			align-items: center;
			float: right;
			padding-right: $uni-spacing-row-base;
		}
	}
</style>
