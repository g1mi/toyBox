<template>
	<view class="cell-page">
		<view class="uv-page__item">
			<text class="uv-page__item__title">ESP32应用</text>
			<uv-cell-group>
				<uv-cell title="OTTO" value="蓝牙控制OTTO" :isLink="true" url="/pages/tools/otto/otto"></uv-cell>
				<!-- <uv-cell icon="" title="WIFI&UDP" value="UDP协议控制元器件" :isLink="true"
					url="/pages/tools/esp32_wifi_udp/esp32_wifi_udp">
				</uv-cell> -->
			</uv-cell-group>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	@import '@/common/demo.scss';
	@import '@/uni_modules/uv-ui-tools/libs/css/color.scss';

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

	.uv-page {
		padding: 0;

		&__item {
			display: grid;
			width: 100%;

			&__title {
				color: $uv-tips-color;
				background-color: $uv-bg-color;
				padding: 15px;
				font-size: 18px;

				&__slot-title {
					color: $uv-primary;
					font-size: 14px;
				}
			}
		}
	}

	.uv-slot-title {
		@include flex;
		flex-direction: row;
		align-items: center;
	}

	.uv-cell-text {
		font-size: 15px;
		line-height: 22px;
		color: #303133;
		margin-right: 5px;
	}

	.uv-slot-value {
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