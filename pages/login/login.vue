<template>
	<kaze-container>
		<kaze-top-bar>
			<template v-slot:right>
				<span class="text-button">注册</span>
			</template>
		</kaze-top-bar>
		<view class="login">
			<image src="../../static/images/avator.jpg" mode="aspectFit"></image>
			<form>
				<input type="text" placeholder="用户名/邮箱" />
				<input type="password" placeholder="密码" />
				<text>{{ tip }}</text>
				<button form-type="submit" @click="tip = tip ? '' : '您输入的用户名/密码有误！'">登录</button>
			</form>
		</view>
	</kaze-container>
</template>

<script>
	export default {
		data() {
			return {
				tip:""
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
.text-button {
	font-size: $uni-font-size-lg;
	font-weight: 500;
	color: $uni-text-color;
	line-height:88rpx;
}

.login {
	padding: 192rpx $uni-spacing-row-base; 
	
	image {
		height: 256rpx;
	}
	
	input {
		margin-top: 40rpx;
		height: 88rpx;
		font-size: $uni-font-size-lg;
		font-weight: 500;
		color: $uni-text-color;
		line-height: 88rpx;
		border-bottom: 1px solid $uni-border-color;
	}
	
	text {
		display: inline-block;
		font-size: $uni-font-size-base;
	}
	
	button {
		margin-top: 80rpx;
		width: 520rpx;
		height: 96rpx;
		background-color: #409EFF;
		color: #fff;
		border-radius: 48rpx;
	}
}
</style>
