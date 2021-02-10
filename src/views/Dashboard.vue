<template>
  <div>

    <base-header class="pb-6 pb-8 pt-5 pt-md-8 bg-white" style="padding-top:49px !important">
      <!-- Card stats -->
      <b-row>
        
         <carousel :per-page="1" :navigate-to="someLocalProperty" :mouse-drag="false">
          <slide>
             <div>
              <img  src="img/content/Group2133.png" style="width:100%;max-height:378px;">
            </div>
          </slide>
          <slide>
           
          </slide>
        </carousel>
      </b-row>
      
    </base-header>

    <!--Charts-->
    <b-container fluid class="mt--7">
      <b-row>
        <b-col cols="8">
          <h3 class="mb-0" style="color:black;font-size:24px;margin-bottom:24px !important">Informasi</h3>
        </b-col>
      </b-row>
      <b-row >
        <b-col xl="4" md="6" >
          <stats-card color="#0036A0" title="2.000"
                      sub-title="Jumlah driver"
          >
          </stats-card>
        </b-col>
        <b-col xl="4" md="6" >
          <stats-card color="#59D185" title="Rp 12.000.0000"
                      sub-title="Total Pengeluaran Bulan Ini"
          >
          </stats-card>
        </b-col>
        <b-col xl="4" md="6" >
          <stats-card color="black" title="200 Jam"
                      sub-title="Total Jam Kerja Bulan Ini"
          >
          </stats-card>
        </b-col>
      </b-row>
      <b-row  style="margin-top:32px">
        <b-col xl="4" md="6" >
          <stats-card color="#0036A0" title="Rp 10.000.000"
                      sub-title="Total Top Up Bulan Ini"
          >
          </stats-card>
        </b-col>
        <b-col xl="4" md="6" >
          <stats-card color="#59D185" title="Rp 2.000.000"
                      sub-title="Total Extra Top Up Bulan Ini"
          >
          </stats-card>
        </b-col>
        <b-col xl="4" md="6" >
          <stats-card color="black" title="200"
                      sub-title="Jumlah PIC"
          >
          </stats-card>
        </b-col>
      </b-row>
      
    </b-container>

  </div>
</template>
<script>
  // Charts
  import * as chartConfigs from '@/components/Charts/config';
  import LineChart from '@/components/Charts/LineChart';
  import BarChart from '@/components/Charts/BarChart';
  import { Carousel, Slide } from 'vue-carousel';

  // Components
  import BaseProgress from '@/components/BaseProgress';
  import StatsCard from '@/components/Cards/StatsCard';

  // Tables
  import SocialTrafficTable from './Dashboard/SocialTrafficTable';
  import PageVisitsTable from './Dashboard/PageVisitsTable';

  export default {
    components: {
      LineChart,
      BarChart,
      BaseProgress,
      StatsCard,
      PageVisitsTable,
      SocialTrafficTable,
      Carousel,
      Slide
    },
    data() {
      return {
        bigLineChart: {
          allData: [
            [0, 20, 10, 30, 15, 40, 20, 60, 60],
            [0, 20, 5, 25, 10, 30, 15, 40, 40]
          ],
          activeIndex: 0,
          chartData: {
            datasets: [
              {
                label: 'Performance',
                data: [0, 20, 10, 30, 15, 40, 20, 60, 60],
              }
            ],
            labels: ['May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
          },
          extraOptions: chartConfigs.blueChartOptions,
        },
        redBarChart: {
          chartData: {
            labels: ['Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
            datasets: [{
              label: 'Sales',
              data: [25, 20, 30, 22, 17, 29]
            }]
          },
          extraOptions: chartConfigs.blueChartOptions
        }
      };
    },
    methods: {
      initBigChart(index) {
        let chartData = {
          datasets: [
            {
              label: 'Performance',
              data: this.bigLineChart.allData[index]
            }
          ],
          labels: ['May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
        };
        this.bigLineChart.chartData = chartData;
        this.bigLineChart.activeIndex = index;
      }
    },
    mounted() {
      this.initBigChart(0);
    }
  };
</script>
<style>
.el-table .cell{
  padding-left: 0px;
  padding-right: 0px;
}
.VueCarousel-pagination{
    bottom: 10px !important;
    position: absolute;
    left: 0 !important;
    width:100px !important
}
.VueCarousel-dot{
    padding:5px !important;
    width:8px!important;
     height:8px!important;
}

</style>
