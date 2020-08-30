<template>
	<image :src="imgSrc" :class="{ 'kaze-avator__small' : size === 'small', 'kaze-avator__circle' : circle }"></image>
</template>

<script>
	export default {
		props: {
			src: {
				type: String,
				default: ''
			},
			size: {
				type: String,
				default: 'small'
			},
			circle: {
				type: Boolean,
				default: false
			}
		},
		data() {
			return {
				imgSrc: this.src
			};
		},
		watch:{
			src(){
				this.imgSrc = this.src
			}
		}
	}
</script>

<style lang="scss">
	.kaze-avator__small {
		width: 68rpx;
		height: 68rpx;
	}
	
	.kaze-avator__circle {
		border-radius: 50%;
	}
</style>
