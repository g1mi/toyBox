<template>
	<view class="u-page">
		<view class="u-page__item">
			<text class="u-page__item__title">ESP32</text>
			<u-gap height="15"></u-gap>
			<u-cell-group>
				<u-cell title="WiFi&UDP" value="UDP协议控制WiFi" :isLink="true"></u-cell>
			</u-cell-group>
		</view>

		<view class="u-page__item">
			<u-gap height="150"></u-gap>
			<u-tabbar :value="value6" @change="name => value6 = name" :fixed="true" :placeholder="true"
				:safeAreaInsetBottom="true" activeColor="#FF7E00">
				<u-tabbar-item text="列表" icon="order"></u-tabbar-item>
				<u-tabbar-item text="需求" icon="plus"></u-tabbar-item>
				<u-tabbar-item text="Bla-bla" icon="chat"></u-tabbar-item>
			</u-tabbar>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				value1: 0,
				value2: 1,
				value3: 'play-right',
				value4: 0,
				value5: 0,
				value6: 0,
				value7: 3
			}
		},
		onLoad() {

		},
		methods: {
			change5(name) {
				if (name === 1) return uni.$u.toast('请您先登录')
				else this.value5 = name
			},
			change1(e) {
				this.value1 = e
				console.log('change1', e);
			},
			click1(e) {
				console.log('click1', e);
			}
		},
	}
</script>

<style lang="scss">
	.cell-page {
		padding-bottom: 20px;
	}

	.cell-box {
		&__title {
			font-size: 14px;
			color: rgb(143, 156, 162);
			margin: 20px 0px 0px 15px;
		}

		&__block {
			// background-color: #fff;
			margin-top: 20px;
		}
	}

	.u-page {
		padding: 0;

		&__item {

			&__title {
				color: $u-tips-color;
				padding: 15px;
				font-size: 24px;

				&__slot-title {
					color: $u-primary;
					font-size: 14px;
				}
			}
		}
	}

	.u-slot-title {
		@include flex;
		flex-direction: row;
		align-items: center;
	}

	.u-cell-text {
		font-size: 15px;
		line-height: 22px;
		color: #303133;
		margin-right: 5px;
	}

	.u-slot-value {
		line-height: 17px;
		text-align: center;
		font-size: 10px;
		padding: 0 5px;
		height: 17px;
		color: #FFFFFF;
		border-radius: 100px;
		background-color: #f56c6c;
	}
</style>