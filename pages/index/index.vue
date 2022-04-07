<template>
	<view>
		<!-- 导航栏 -->
		<u-navbar :bgColor="bgColor" placeholder>

			<view class="u-nav-slot nav_txt" slot="left">
				<text class="front_size_nav" style="display: flex;">上海</text>
				<u-icon name="arrow-right" color="#2979ff" size="24"></u-icon>
			</view>

			<view class="u-nav-slot " slot="right">
				<view class="u-page__tag-item">
					<u-search></u-search>
				</view>
			</view>
		</u-navbar>
		<!-- 求助墙 -->
		<view class="help_wall">

		</view>

		<u-gap height="10"></u-gap>

		<view style="display: flex;justify-content: center;">

			<u-subsection :list="list" mode="button" :current="current" @change="change" fontSize=16 bgColor='#F8F8F8'></u-subsection>
		</view>

		<u-gap height="10"></u-gap>
		<view v-if="current==0"><help></help></view>
		<view v-else-if="current==1"><dongTau ></dongTau></view>
		
	<uni-fab ref="fab" :pattern="pattern"  :horizontal="horizontal" 
	@fabClick="fabClick" />

	</view>
</template>

<script>
	import dongTai from '../../components/dongTau/dongTau.vue'
	import help from '../../components/help/help.vue'
	export default {
		components:{dongTai,help},
		data() {
			return {
				bgColor: "#F8F8F8",
				list: [{
						name: '求助'
					},
					{
						name: '动态',
					}, {
						name: '寻根',
					}, {
						name: '他乡遇故'
					},
				],
				current: 0,
				horizontal: 'right',
				pattern: {
					buttonColor: '#fffff',
				},
			};
		},
		onLoad() {

		},
		methods: {

			click() {},
			change(index) {
				this.current = index
			},
			onClick(e) {
				console.log(e)
			},
			actionsClick(text) {
				uni.showToast({
					title: text,
					icon: 'none'
				})
			},
			fabClick() {
				uni.navigateTo({
					url: 'publish_help/publish_help'
				});
			},
		}
	}
</script>

<style lang="scss" scoped>
	.front_size_nav {
		font-size: 35rpx;
	}

	.nav_txt {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.help_wall {
		display: flex;
		flex-direction: column;
		height: 450rpx;
		background: url(../../static/wall_image/3e03e9c2473c40b180aa99a37c0589fa.jpg) -600px -864px no-repeat;
	}

</style>
