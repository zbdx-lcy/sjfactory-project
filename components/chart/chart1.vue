<template>
	<!-- 能用了就是图表没弄好 -->
	<canvas ref="pieChart"></canvas>
</template>

<script>
	import Chart from 'chart.js/auto';

	export default {
		name: "chart1",
		data() {
			return {
				pieChartData: {
					labels: ['完好', '破损'],
					datasets: [{
						label: '沙棘果总数',
						data: [70, 30 /* 在这里填入沙棘果完好和破损的具体数据 */ ],
						backgroundColor: [
							'rgba(75, 192, 192, 0.5)',
							'rgba(255, 99, 132, 0.5)',
						],
						borderColor: [
							'rgba(75, 192, 192, 1)',
							'rgba(255, 99, 132, 1)',
						],
						borderWidth: 1,
					}, ],
				},
			};
		},
		mounted() {
			this.renderPieChart();
		},
		methods: {
			renderPieChart() {
			        this.$nextTick(() => {
			            const ctx = this.$refs.pieChart.getContext('2d');
			            new Chart(ctx, {
			                type: 'pie',
			                data: this.pieChartData,
			            });
			        });
			    },
		},
	};
</script>