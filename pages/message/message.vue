<template>
	<view class="main">
		<u-tabs :list="list" @click="change"
		
		></u-tabs>
		<view v-if="current==0"><friends></friends></view>
		<view v-else-if="current==1"></view>
		
	</view>
</template>

<script>
	import friends from '../../components/message/friends.vue'
	export default {
		components:{friends},
		data() {
			return {
				list:[
					{name:'通讯录'},
					{name:'消息'}
				],
				current:0
			}
		},
		methods: {
			change(select){
				this.current=select.index
			}
		}
	}
</script>

<style lang="scss" scoped>


</style>
