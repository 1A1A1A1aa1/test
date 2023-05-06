<template>
	<view class="index">
		<u-navbar :placeholder="true" :autoBack="true">
			<view class="left" slot="left">
				<u-icon name="arrow-leftward" size="40rpx"></u-icon>&nbsp;back
			</view>
			<view class="right" slot="right">
				<u-icon name="more-circle-fill"></u-icon>
				<u-icon name="search"></u-icon>
				<u-icon name="bag-fill"></u-icon>
			</view>
		</u-navbar>
		<view class="Headpicture">
			<view class="left">
				<u-avatar size="100rpx"></u-avatar>
				<view class="information">
					<view class="name">McDonald's</view>
					<view class="address"><u-icon name="map"></u-icon>Bramlea Sandalwood</view>
				</view>
			</view>
			<view class="">
				<u-avatar size="100rpx"></u-avatar>
			</view>
		</view>
		<view class="tabs">
			<u-tabs lineColor="#484c51" lineWidth="60" :list="list1" @click="click"></u-tabs>
		</view>
		<view class="content">
			<view class="top">
				<view class="btn activebtn">Today's Deals</view>
				<view class="btn">Burger Meals</view>
				<view class="btn">Chicken Fish</view>
			</view>
			<view class="list">
				<view class="left">
					<u-avatar size="100rpx"></u-avatar>
					<view class="information">
						<view class="">Classic Cheese Burger</view>
						<view class="">(400 Cals)</view>
						<view class="price">
							<view class="void">$5.89</view>
							<view class="effective">$4.23</view>
						</view>
					</view>
				</view>
				<u-icon name="arrow-right" size="40rpx"></u-icon>
			</view>
			<view class="list">
				<view class="left">
					<u-avatar size="100rpx"></u-avatar>
					<view class="information">
						<view class="">Classic Cheese Burger</view>
						<view class="">(400 Cals)</view>
						<view class="price">
							<view class="void">$5.89</view>
							<view class="effective">$4.23</view>
						</view>
					</view>
				</view>
				<u-icon name="arrow-right" size="40rpx"></u-icon>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list1: [{
					name: 'Breakfast Menu',
				}, {
					name: 'Lunch & Dinner',
				}, {
					name: 'Lunch Dinner'
				}],
				
			}

		},
		methods: {
			click(item) {
				console.log('item', item);
			}
		}
	}
</script>
<style lang="scss">
	.index {
		.left {
			display: flex;
		}
		.list:nth-child(n+3){
			border-top: #46515d solid 2rpx;
		}
		.list{
			padding: 40rpx 30rpx 30rpx;
			display: flex;
			justify-content: space-between;
			align-items: center;
			height: 150rpx;
			.left{
				display: flex;
				align-items: center;
			}
			.information{
				margin-left: 20rpx;
				.price{
					display: flex;
					font-size: 30rpx;
					.void{
						text-decoration: line-through;
					}
					.effective{
						font-weight: bold;
						color: 	#64c4ed;
						margin-left: 10rpx;
					}
				}
			}
		}
		.content {
			margin-top: 20rpx;
			.top{
				width: 100%;
				box-sizing: border-box;
				padding: 0 20rpx;
				display: flex;
				justify-content: space-between;
				.btn{
					font-size: 30rpx;
					border-radius: 50rpx;
					width: 220rpx;
					height: 80rpx;
					line-height: 80rpx;
					text-align: center;
					color: #c5cfd8;
					background-color: #eef2f5;
				}
				.activebtn{
					color: white;
					transform: scale(1.1);
					background-color: #46515d;
				}
			}
		}

		.tabs {
			height: 120rpx;
			background-color: #eef2f5;
			display: flex;
			align-items: center;
		}

		.Headpicture {
			display: flex;
			justify-content: space-between;
			width: 100%;
			box-sizing: border-box;
			padding: 40rpx 30rpx 30rpx;

			.left {
				display: flex;

				.information {
					margin-left: 20rpx;
					display: flex;
					flex-direction: column;
					justify-content: space-between;

					.name {
						font-weight: bold;
						font-size: 40rpx;
					}
				}

				.address {
					font-size: 30rpx;
					display: flex;
				}
			}
		}

		.right {
			width: 200rpx;
			display: flex;
			justify-content: space-between;
		}
	}
</style>