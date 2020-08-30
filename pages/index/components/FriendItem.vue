<template>
	<view class="friend-item">
		<view class="friend-item-avator">
			<text class="friend-item-avator-badge">{{ badgeNumber }}</text>
			<image
				:src="avatorSrc"
				class="friend-item-avator-image"
			>
			</image>
			</uni-badge>
		</view>
		<view class="friend-item-info">
			<view class="friend-item-info__top">
				<view class="nickname">
					<text> {{ nickName }} </text>
				</view>
				<view class="time">
					<text> {{ lastReplyTime }}</text>
				</view>
			</view>
			<view class="friend-item-info__bottom">
				<text class="message">{{ lastMessage }}</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			avator: {
				type: String,
				default: null
			},
			badge: {
				type: Number,
				default: null
			},
			nickname: {
				type: String,
				default: null
			},
			time: {
				type: String,
				default: null
			},
			message: {
				type: String,
				default: null
			}
		},
		data() {
			return {
				avatorSrc:this.avator,
				badgeNumber: this.badge,
				nickName: this.nickname,
				lastReplyTime: this.time,
				lastMessage: this.message,
			};
		}
	}
</script>

<style lang="scss">
	.friend-item {
		height: 140rpx;
		box-sizing: border-box;
		padding: 16rpx $uni-spacing-row-base; 
		
		.friend-item-avator {
			position: relative;
			float: left;
			
			.friend-item-avator-image {
				height: 96rpx;
				width: 96rpx;
				border-radius: 16rpx;
			}
			
			.friend-item-avator-badge {
				position: absolute;
				z-index: 10;
				top: -6rpx;
				left: 68rpx;
				height: 36rpx;
				min-width: 36rpx;
				background-color: #FF0000;
				border-radius: $uni-border-radius-circle;
				line-height: 36rpx;
				color: $uni-text-color-inverse;
				font-size: $uni-font-size-sm;
				text-align: center;
				
			}
		}
		
		.friend-item-info {
			padding-left: 128rpx;
			
			.friend-item-info__top {
				height: 50rpx;
				.nickname {
					float:left;
					font-size: $uni-font-size-lg;
					font-weight: 400;
					color:black;
					line-height: 50rpx;
				}
				
				.time {
					float:right;
					font-size: $uni-font-size-sm;
					color: $uni-text-color-disable;
					line-height: 50rpx;
				}
			}
			
			.friend-item-info__bottom {
				.message {
					display: -webkit-box;
					-webkit-box-orient: vertical;
					-webkit-line-clamp: 1;
					overflow: hidden;
					line-height: 40rpx;
					font-size: $uni-font-size-base;
					font-weight: 400;
					color:$uni-text-color-disable;
				}
			}
		}
	}
</style>
