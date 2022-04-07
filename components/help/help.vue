<template>
	<view>
		<uni-card @click="To_Info">


			<view class="header">
				<image class="img" :src="cardinfo.authImg"></image>
				<view class="auth">{{cardinfo.authName}}</view>
				<view class="leave">LV{{cardinfo.leave}}</view>
				<view class="tag">{{cardinfo.tag}}</view>
				<view class="time">{{cardinfo.createTime}}</view>

			</view>

		<u-gap height="10"></u-gap>
			<text class="help_title"> 求帮忙！！！！！！！</text>

			<text class="help_constant u-line-2">有没有人有青菜！家里没菜了！！！家里没菜了！！！家里没菜了！！！家里没菜了！！！想吃肉</text>
			<view slot="actions" class="card-actions">

				<view class="card-actions-item" @click="actionsClick('点赞')">
					<uni-icons type="heart" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">点赞</text>
				</view>
				<view class="card-actions-item" @click="actionsClick('评论')">
					<uni-icons type="chatbubble" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">详情</text>
				</view>
			</view>
		</uni-card>

		<card :cardinfo="cardinfo"></card>

	</view>
</template>

<script>
	export default {
		name: "help",

		data() {
			return {
				cardinfo: {
					"authImg": 'https://cdn.uviewui.com/uview/album/1.jpg',
					"authName": "王五",
					"createTime": "2022-04-07",
					"content": " 内容",
					"goodNum": "22",
					"leave": 8,
					"tag": "求助"
				}
			};
		},
		methods: {
			To_Info() {
				uni.navigateTo({
					url: '../../pages/index/help_info/help_info'
				});
			}
		}
	}
</script>

<style lang="scss" scoped>
	.help_title {
		display: flex;
		font-size: 40rpx;
		font-weight: 1000;
	}

	.card-actions {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		align-items: center;
		height: 45px;
		border-top: 1px #eee solid;
	}

	.card-actions-item {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.card-actions-item-text {
		font-size: 12px;
		color: #666;
		margin-left: 5px;
	}

	.header {}

	.img {
		margin: 20upx 0px 20upx 10upx;
		height: 90upx;
		width: 90upx;
		border-radius: 90upx;
		border: 1px solid #007AFF;
		display: inline-flex;
	}

	.auth {
		font-weight: bolder;
		font-family: Arial, Helvetica, sans-serif;
		font-size: 15px;
		margin-top: -100upx;
		margin-left: 130upx;
	}

	.time {
		font-family: Arial, Helvetica, sans-serif;
		font-size: 12px;
		display: inline-flex;
		margin-left: 130upx;
		margin-top: -20upx;
		color: #808080;
	}

	.leave {
		font-size: 12px;
		text-align: center;
		background: #4CD964;
		width: 75upx;
		text-align: center;
		height: 35upx;
		border-radius: 20upx;
		color: #F2F2F2;
		margin-left: 210upx;
		margin-top: -35upx;
	}

	.tag {
		font-size: 12px;
		text-align: center;
		background: #36BBFF;
		width: 120upx;
		text-align: center;
		height: 35upx;
		border-radius: 10upx;
		color: #F2F2F2;
		margin-left: 300upx;
		margin-top: -36upx;
	}
</style>
