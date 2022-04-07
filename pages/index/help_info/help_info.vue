<template>
	<view class="main">
		<uni-card >
			<view class="user">
				<u-avatar src='https://cdn.uviewui.com/uview/album/1.jpg'></u-avatar>
				<view>
					<text class="user_name">
						王五
					</text>
					<text class="help_date">4-07</text>
				</view>
			</view>
			<view class="help_info">
				<text class="help_title">求帮忙！！！！！！！</text>
				<u-gap height="15"></u-gap>
				<text class="help_detail">有没有人有青菜！家里没菜了！！！家里没菜了！！！家里没菜了！！！家里没菜了！！！想吃肉</text>
			</view>
		</uni-card>



		<uni-card is-full>
			<comment :articleId="'article1'"></comment>
		</uni-card>

	</view>
</template>

<script>
	import comment from '../../../components/Comment/Comment.vue'
	export default {
		components: {
			comment
		},
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss" scoped>
	.main {
		display: flex;
		flex-direction: column;

		.user {
			display: flex;
			align-items: center;

			.user_name {
				display: flex;
				flex-direction: column;

				margin-left: 10rpx;
				font-size: 34rpx;
				font-weight: 600;
			}

			.help_date {
				margin-left: 20rpx;
			}
		}
	}

	.help_info {
		margin-top: 20rpx;
		padding-top: 10rpx;
		border-top: 5rpx solid;
	}

	.help_title {
		display: flex;
		font-size: 40rpx;
		font-weight: 700;
	}

	.help_detail {

		font-size: 30rpx;
		font-weight: 600;
	}

	.chat-custom-right {
		flex: 1;
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: column;
		justify-content: space-between;
		align-items: flex-end;
	}

	.chat-custom-text {
		font-size: 12px;
		color: #999;
	}
</style>
