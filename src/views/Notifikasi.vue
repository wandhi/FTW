<template>
  <div>

    <base-header class="pb-6 pb-8 pt-5 pt-md-8 bg-white" style="padding-top:49px !important">
      <!-- Card stats -->
      <b-row>
       
      </b-row>
      
    </base-header>

    <!--Charts-->
    <b-container fluid class="mt--7">
      <b-row>
        <b-col cols="8">
          <h3 class="mb-0" style="color:black;font-size:16px;margin-bottom:24px !important;font-weight:500">Notifikasi</h3>
        </b-col>
      </b-row>
      <b-row style="display:flex;justify-content:flex-start;align-items:center;">
       <b-col cols="12">
          <h3 class="mb-0" style="color:black;font-size:16px;margin-bottom:16px !important;font-weight:500">Hari Ini</h3>
        </b-col>
      </b-row>
        <notif-card code="1232" driver="Reza Ahmad" time="09.00" date="10/12/2020" type="pengeluaran" pengeluaran="bensin" total="Rp.200.000">
        </notif-card>
        <notif-card code="1232" driver="Reza Ahmad" time="09.00" date="10/12/2020"  type="absen" absenMasuk="12/11/2021|09.00" absenPulang="12/11/2021|09.00" total="Rp.200.000">
        </notif-card>
        <notif-card code="1232" driver="Reza Ahmad" time="09.00" date="10/12/2020" type="izin" tanggalIzin="12/11/2021|09.00">
        </notif-card>
        <notif-card code="1232" driver="Reza Ahmad" time="09.00" date="10/12/2020" type="libur" tanggalLibur="12/11/2021|09.00">
        </notif-card>
        <b-row style="margin-top:55px">
           
         
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
  import NotifCard from '@/components/Cards/NotifCard';

  // Tables
  import SocialTrafficTable from './Dashboard/SocialTrafficTable';
  import PageVisitsTable from './Dashboard/PageVisitsTable';

  export default {
    components: {
      NotifCard,
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
.dropDwn{
  background:rgba(0, 54, 160, 0.1);
  color:pink
}
.nav-pills .nav-link.active, .nav-pills .show > .nav-link {
    color:#5e72e4;
    background-color: #5e72e400;
    border:0px;
    border-radius: 0;
    box-shadow: none;
    border-bottom: 1px solid #5e72e4;
}
.card-header {
    padding-top: 0;
    padding-bottom: 0;
   
}
.nav-pills .nav-link {
  box-shadow:none;
  color:black
}
.button-c1{
  padding:7px;
  background: #0036A0;
  border-radius: 4px;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 16px;
  color:white;
  font-family: Poppins;
  width:158px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.flex-row{
  display: flex;
  flex-direction: row;
}
.flex-col{
  display: flex;
  flex-direction: column;
}
.flex-center{
  justify-content: center;
  align-items: center;
}

.btn-group .btn, .input-group .btn {
    margin-right: 0;
    -webkit-transform: translateY(0);
    transform: translateY(0);
    box-shadow: none !important;
    background:rgba(0, 54, 160, 0.1);
    min-width:125px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color:#0036A0;
    font-size: 12px;
    height: 24px;
    font-weight:normal

}
</style>
