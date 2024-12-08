<script>
    import { Chart, Card, A, Button, Dropdown, DropdownItem, Popover, Tooltip, Heading, P } from 'flowbite-svelte';
    import { InfoCircleSolid, ArrowDownToBracketOutline, ChevronDownOutline, ChevronRightOutline, PenSolid, DownloadSolid, ShareNodesSolid } from 'flowbite-svelte-icons';
  
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
            return value ;
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
  
  <Card>
    <div class="flex justify-between items-start w-full">
      <div class="flex-col items-center">
        <div class="flex items-center mb-1">
          <h5 class="text-xl leading-none text-gray-900 dark:text-white me-1">Business Relation Types</h5>
        </div>
      </div>
    </div>
  
    <Chart {options} class="py-6" />
  
    <div class="grid grid-cols-1 items-center border-gray-200 border-t dark:border-gray-700 justify-between">
      <div class="flex justify-between items-center pt-5">
        
        <A href="/businessrelations" class="uppercase text-sm hover:text-primary-700 dark:hover:text-primary-500 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700 px-3 py-2 hover:no-underline">
          See Business Relations
          <ChevronRightOutline class="w-2.5 h-2.5 ms-1.5" />
        </A>
      </div>
    </div>
  </Card>
</div>