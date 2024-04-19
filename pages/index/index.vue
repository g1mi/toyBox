<template>
	<view class="u-page">
		<view class="u-page__item">
			<text class="u-page__item__title">ESP32</text>
			<u-gap height="15"></u-gap>
			<u-cell-group>
				<u-cell title="WiFi&UDP" value="UDP协议控制元器件" :isLink="true" url="/pages/tools/esp32_wifi_udp/esp32_wifi_udp"></u-cell>
			</u-cell-group>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {
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