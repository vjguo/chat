<template>
	<kaze-container>
		<kaze-top-bar>
			<template v-slot:left>
				<kaze-avator :src="avator" size="small" circle></kaze-avator>
			</template>
			<template v-slot:center>
			</template>
			<template v-slot:right>
				<i class="fa fa-plus fa-lg"></i>
			</template>
		</kaze-top-bar>
		<view class="friend-list">
			<FriendItem
				v-for="friendItem in friendItems"
				:key="friendItem.id"
				:avator="friendItem.avator"
				:badge="friendItem.badge"
				:nickname="friendItem.nickname"
				:message="friendItem.message"
				:time="friendItem.time"
			>
			</FriendItem>
		</view>
	</kaze-container>
</template>

<script>
	import FriendItem from './components/FriendItem.vue'
	export default {
		components: {
			FriendItem
		},
		data() {
			return {
				avator:'../../static/images/avator.jpg',
				friendItems: [
					{
						id: 0,
						avator: '../../static/images/avator.jpg',
						badge: 309,
						nickname: 'Nick Name',
						message: 'This is message aa啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊.',
						time: 'PM 7:00'
					},
					{
						id: 1,
						avator: '../../static/images/avator.jpg',
						badge: 4,
						nickname: 'Nick Name',
						message: 'This is message.',
						time: 'PM 7:00'
					},
					{
						id: 2,
						avator: '../../static/images/avator.jpg',
						badge: 4,
						nickname: 'Nick Name',
						message: 'This is message.',
						time: 'PM 7:00'
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
</style>
