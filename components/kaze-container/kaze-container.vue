<template>
	<view class="content">
		<view class="main">
			<slot></slot>
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
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		// 解决手机顶部状态栏内容被覆盖
		// padding-top: var(--status-bar-height);
		padding-bottom: $uni-spacing-col-base;
	}

	.main {
		box-sizing: border-box;
		margin-top: 89rpx;
		width: 100%;
	}
</style>
