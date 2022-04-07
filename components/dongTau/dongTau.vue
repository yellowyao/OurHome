<template>
	<view>
		<uni-card padding="10px 0" style="display: flex; flex-direction: column;" v-for="i in 2" :key='i'>
			<template v-slot:title>
				<view class="user_image">
					<u-avatar src='https://cdn.uviewui.com/uview/album/7.jpg'></u-avatar>
					<text class="user_text">{{listname[0]}}</text>
				</view>
			</template>
			
			<text class="uni-body uni-mt-5 u-line-5">
				<img style="width: 99%; height: 450rpx;" :src="cover"></img>
				我家两只猫，大猫间歇性黏人，二猫长期黏人据我观察，它们最明显的差别就是黏人的小猫咪求摸/求抱都很主动，甚至会主动露出肚皮让人摸到爪子在空中踩奶二猫的妈妈放出笼子就往人身上扒拉，拔都拔不下来鉴于某些宠物店不让人摸猫（为了猫和人的安全），
				在选小猫的时候当然是问店主更好啦～
				（此处提醒：宠物店买猫也要签合同，考察宠物店环境，考察宠物店主人品，考察小动物的屎盆子、饭盆、水，多看几次再买，不要头脑一热就定下来）
			</text>
			<view slot="actions" class="card-actions">
				<view class="card-actions-item" @click="actionsClick('分享')">
					<uni-icons type="pengyouquan" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">分享</text>
				</view>
				<view class="card-actions-item" @click="actionsClick('点赞')">
					<uni-icons type="heart" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">点赞</text>
				</view>
				<view class="card-actions-item" @click="actionsClick('评论')">
					<uni-icons type="chatbubble" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">评论</text>
				</view>
			</view>
		</uni-card>








	</view>
</template>

<script>
	export default {
		name: "dongTau",
		data() {
			return {
				listname: [
					'张三',
					'李四',
					'王五',
					'赵六',

				],
				cover: 'https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/094a9dc0-50c0-11eb-b680-7980c8a877b8.jpg',
				avatar: 'https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png',
				extraIcon: {
					color: '#4cd964',
					size: '22',
					type: 'gear-filled'
				}
			};
		}
	}
</script>

<style lang="scss" scoped>
	.user_text {
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 45rpx;
		font-weight: 700;
		margin-left: 10rpx;
	}

	.uni-card__content {
		display: flex;
	}

	.user_image {
		display: flex;
		margin-top: 15rpx;

	}

	.container {
		overflow: hidden;
	}

	.custom-cover {
		flex: 1;
		flex-direction: row;
		position: relative;
	}

	.cover-content {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		height: 40px;
		background-color: rgba($color: #000000, $alpha: 0.4);
		display: flex;
		flex-direction: row;
		align-items: center;
		padding-left: 15px;
		font-size: 14px;
		color: #fff;
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

	.cover-image {
		flex: 1;
		height: 150px;
	}

	.no-border {
		border-width: 0;
	}
</style>
