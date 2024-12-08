<script>
	import {
		Chart,
		Card,
		A,
		Button,
		Dropdown,
		DropdownItem,
		Popover,
		Tooltip,
		Heading,
		P
	} from 'flowbite-svelte';
	import {
		InfoCircleSolid,
		ArrowDownToBracketOutline,
		ChevronDownOutline,
		ChevronRightOutline,
		PenSolid,
		DownloadSolid,
		ShareNodesSolid
	} from 'flowbite-svelte-icons';

	const options = {
		series: [18, 7, 4, 2],
		colors: ['#1C64F2', '#16BDCA', '#FDBA8C', '#E74694'],
		chart: {
			height: 320,
			width: '100%',
			type: 'donut'
		},
		stroke: {
			colors: ['transparent'],
			lineCap: ''
		},
		plotOptions: {
			pie: {
				donut: {
					labels: {
						show: true,
						name: {
							show: true,
							fontFamily: 'Inter, sans-serif',
							offsetY: 20
						},
						total: {
							showAlways: true,
							show: true,
							label: 'Total Business Relations',
							fontFamily: 'Inter, sans-serif',
							formatter: function (w) {
								const sum = w.globals.seriesTotals.reduce((a, b) => {
									return a + b;
								}, 0);
								return `${sum}`;
							}
						},
						value: {
							show: true,
							fontFamily: 'Lexend',
							offsetY: -20,
							formatter: function (value) {
								return value;
							}
						}
					},
					size: '80%'
				}
			}
		},
		grid: {
			padding: {
				top: -2
			}
		},
		labels: ['Clients', 'Suppliers', 'Service Relations', 'Research Cooperations'],
		dataLabels: {
			enabled: false
		},
		legend: {
			position: 'bottom',
			fontFamily: 'Inter, sans-serif'
		},
		yaxis: {
			labels: {
				formatter: function (value) {
					return value;
				}
			}
		},
		xaxis: {
			labels: {
				formatter: function (value) {
					return value;
				}
			},
			axisTicks: {
				show: false
			},
			axisBorder: {
				show: false
			}
		}
	};
</script>

<div>
	<Card class="bg-opacity-20">
		<div class="flex w-full items-start justify-between">
			<div class="flex-col items-center">
				<div class="mb-1 flex items-center">
					<h5 class="me-1 text-xl leading-none text-gray-900 dark:text-white">
						Business Relation Types
					</h5>
				</div>
			</div>
		</div>

		<Chart {options} class="mb-4 size-60 py-6" />
	</Card>
</div>
