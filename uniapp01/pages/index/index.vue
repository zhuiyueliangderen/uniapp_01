<template>
	<view>
		<!--首页顶部导航-->
		<navigator url="/HuoDong/ZhuanTi/WeiShouDanTheme/" target="_blank" id="topbanner">
			<view class="headBg"></view>
		</navigator>
		<!--停单提示 topbar-->
		<view class="site-nav">
			<view class="container">
				<uni-list class="site-nav-l">
					<uni-list-item class="menu">
						<navigator url="/" onclick="addfavorite();return false;">
							<text class="ico ico-star"></text>
							收藏鲜花网(hua.com)
						</navigator>
					</uni-list-item>
					<uni-list-item class="menu dropdown">
						<navigator url="javascript:void(0)">
							<text class="ico ico-weixin"></text>
							关注微信
						</navigator>
						<view class="dropdown-menu dropdown-weixin">
							<image src="/static/images/index/wechat_qrcode.jpg.png" alt=""></image>
							<text>扫码关注<br>回复"礼物"更多惊喜！</text>
						</view>
					</uni-list-item>
					<uni-list-item class="menu dropdown">
						<navigator url="/mobile/" target="_blank">
							<text class="ico ico-mobile"></text>
							花礼网app
						</navigator>
						<view class="dropdown-menu dropdown-weixin">
							<image src="/static/images/index/app_qrcode.jpg.png" mode=""></image>
							<text>新人专享100元APP礼包</text>
						</view>
					</uni-list-item>
				</uni-list>
			</view>
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

		}
	}
</script>

<style lang="scss">
	.headBg{
		height: 80upx;
		background: url('https://img02.hua.com/pc/images/pc_newuser_order_100.png?') 50% 0px no-repeat;
	}
	.site-nav {
	    font-size: 12px;
	    min-width: 1200px;
	    height: 35upx;
	    border-bottom: 1px solid #e6e6e6;
	    background-color: #f2f2f2;
		.container {
		    width: 1200px;
		    max-width: none !important;
		    padding-right: 0;
		    padding-left: 0;
			.site-nav-l {
			    float: left;
				.menu {
				    line-height: 34px;
				    display: block;
				    float: left;
					navigator {
					    position: relative;
					    display: block;
					    height: 35px;
					    padding: 0 8px;
						.ico {
							display: inline-block;
							vertical-align: middle;
						    margin-right: 2px;
						}
						.ico-star,.ico-weixin,.ico-mobile{
							width: 24px;
							height: 24px;
							background:url('/static/images/index/common_z.png') no-repeat;;
							background-position: 0px -318px;
							
						}
						.ico-weixin,.ico-mobile{
							background-position: -374px -131px;
							margin-top: -1upx;
						}
						.ico-mobile{
							background-position: -294px -171px;
						}
					}
				}
				.dropdown {
				    position: relative;
					navigator{
						z-index: 1001;
						margin-top: -1px;
						margin-bottom: -1px;
						border: 1px solid transparent;
						border-bottom: 0;
					}
					.dropdown-menu {
					    font-size: 12px;
					    margin: 0;
					    padding: 10px;
					    border: 1px solid #d9d9d9;
					    border-radius: 0;
						text{
							margin-top: 10px;
							margin-bottom: 0;
						}
					}
					.dropdown-weixin {
					    line-height: 18px;
					    min-width: 160px;
					    padding-top: 20px;
					    text-align: center;
						image{
							width: 124upx;
							height: 124upx
						}
					}
				}
			}
		}
	}
</style>
