<template>
	<view class="home-page">
		<!-- 基本数据 -->
		<!-- /基本数据 -->
		<!-- 服务占比 -->
		<qiun-data-charts type="pie" :chartData="pieChartData" />
		<qiun-data-charts type="pie" :chartData="pieChartData" />
		<!-- /服务占比 -->
		<!-- 流量统计 -->
		<qiun-data-charts type="demotype" :chartData="chartData" />
		<!-- /流量统计 -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				chartData:{
				  categories: ["2016", "2017", "2018", "2019", "2020", "2021"],
				  series: [{
				    name: "目标值",
				    data: [35, 36, 31, 33, 13, 34]
				  }, {
				    name: "完成量",
				    data: [18, 27, 21, 24, 6, 28]
				  }]
				},
				pieChartData: {
					series: [
					        {
					            data: [
					                {
					                    name: "一班",
					                    value: 50
					                },
					                {
					                    name: "二班",
					                    value: 30
					                },
					                {
					                    name: "三班",
					                    value: 20
					                },
					                {
					                    name: "四班",
					                    value: 18
					                },
					                {
					                    name: "五班",
					                    value: 8
					                }
					            ]
					        }
					    ]
				}
			};
		}
	}
</script>

<style lang="scss">
.home-page {
	width: 100%;
	padding: 0 5rpx;
} 
</style>
