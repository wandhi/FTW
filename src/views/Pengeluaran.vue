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
          <h3 class="mb-0" style="color:black;font-size:16px;margin-bottom:24px !important;font-weight:500">Pengeluaran</h3>
        </b-col>
      </b-row>
      <b-row style="display:flex;justify-content:flex-start;align-items:center">
        <b-col xl=2>
          <b-dropdown id="dropdown-1" text="PIC" style="min-width:125px" >
            <b-dropdown-item>
              <span style="font-size :10px;color: #A8A8A8">PIC1234</span>
              <br>
              <span>Fariz Ramadhan</span>
            </b-dropdown-item>
            <b-dropdown-item>
              <span style="font-size :10px;color: #A8A8A8">PIC1234</span>
              <br>
              <span>Fariz Ramadhan</span>
            </b-dropdown-item>
            <b-dropdown-item>
              <span style="font-size :10px;color: #A8A8A8">PIC1234</span>
              <br>
              <span>Fariz Ramadhan</span>
            </b-dropdown-item>
            
          </b-dropdown>
        </b-col>
        <b-col xl=6 style="display:flex;flex-direction:row;justify-content:center;align-items:center">
          <img src="img/icons/sidebar/search.png" style="margin-right:15px;width:12px;height:12px;object-fit:content"/><b-form-input id="input-small" size="sm" placeholder="Cari kode driver atau nama driver" style="border:0 !important;font-size:12px"></b-form-input>
        </b-col>
        <b-col lg="4" class="pb-2 "><b-button size="sm" class="button-c1"><span><img src="img/icons/sidebar/download.png" style="margin-right:15px;width:20px;height:20px">Download</span></b-button></b-col>
      </b-row>
      <b-row>
        
      </b-row>
        <b-row style="margin-top:55px">
          <b-col>
            <b-card no-body style="border:0">
              <b-tabs pills card>
                
                <b-tab title="Detail Pengeluaran" active>
                  <b-row>
                    <b-col>
                      <span style="font-size:14px;color:#333335">Detail Pengeluaran Driver</span>
                    </b-col>
                  </b-row>
                  <b-row style="padding-top:41px;padding-bottom:41px">
                    <b-col xl=4 style="display:flex;justify-content:center;align-items:center;">
                      <span style="font-size:14px">Kode</span>
                    </b-col>
                    <b-col xl=8>
                      <span style="font-size:14px">: D12387
                      </span>
                    </b-col>
                    <b-col xl=4 style="display:flex;justify-content:center;align-items:center;">
                      <span style="font-size:14px">Nama</span>
                    </b-col>
                    <b-col xl=8>
                      <span style="font-size:14px">: Fariz Ramadhan</span>
                    </b-col>
                  </b-row>
                  <b-row >
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  sub-title="Total Pengeluaran"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#FD8C8C" title="Rp 2.000.000"
                                  sub-title="Saldo Saat Ini"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  sub-title="Unit Bulanan"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                  <b-row  style="margin-top:32px">
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  sub-title="Saldo Minimum"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  label="admin"
                                  labelColor="#0036A0"
                                  bottomText="Topup"
                                  sub-title="Andriansyah - AD3789"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  sub-title="Saldo Awal"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                  <b-row  style="margin-top:32px">
                    <b-col xl="4" md="6" >
                      <stats-card color="black" title="24 jam"
                                  sub-title="Max Waktu Scan"
                      >
                      </stats-card>
                    </b-col>
                  <b-col xl="4" md="6" >
                      <stats-card color="black" title="24 jam"
                                  sub-title="Max Waktu Response"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="black" title="24 jam"
                                  sub-title="Max Waktu Transfer"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                  <b-row  style="margin-top:32px">
                    <b-col xl="4" md="6" >
                      <stats-card color="#0036A0" title="2 November 2019"
                                  sub-title="Start Periode"
                      >
                      </stats-card>
                    </b-col>
                  <b-col xl="4" md="6" >
                      <stats-card color="#0036A0" title="1 Desember 2019"
                                  sub-title="Max Waktu Response"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#0036A0" title="2"
                                  sub-title="Siklus Tanggal"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                </b-tab>
                <b-tab title="Topup">

                    <b-row>
                    <b-col>
                      <span style="font-size:14px;color:#333335">Detail Pengeluaran Driver</span>
                    </b-col>
                  </b-row>
                  <b-row style="padding-top:41px;padding-bottom:41px;margin-left:10%">
                    <b-col xl=4 style="display:flex;justify-content:flex-start;text-align:left; align-items:center;">
                      <span style="font-size:14px">Kode</span>
                    </b-col>
                    <b-col xl=8>
                      <span style="font-size:14px">: D12387
                      </span>
                    </b-col>
                    <b-col xl=4 style="display:flex;justify-content:flex-start;text-align:left; align-items:center;">
                      <span style="font-size:14px">Nama</span>
                    </b-col>
                    <b-col xl=8>
                      <span style="font-size:14px">: Fariz Ramadhan</span>
                    </b-col>
                    <b-col xl=4 style="display:flex;justify-content:flex-start;text-align:left; align-items:center;">
                      <span style="font-size:14px">Siklus Tanggal</span>
                    </b-col>
                    <b-col xl=8>
                      <span style="font-size:14px">: 20</span>
                    </b-col>
                  </b-row>
                  <b-row >
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  sub-title="Topup"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#FD8C8C" title="Rp 2.000.000"
                                  sub-title="Saldo Saat Ini"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Rp 2.000.000"
                                  sub-title="Saldo Minimum"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                  <b-row  style="margin-top:32px">
                    <b-col xl="4" md="6" >
                      <stats-card color="black" title="12"
                                  sub-title="Top up ke- Bulan ini"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="black" title="BCA"
                                  labelColor="#0036A0"
                                  sub-title="Bank"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="#59D185" title="Dimas Danang R"
                                  sub-title="Nama Rekening"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                  <b-row  style="margin-top:32px">
                    <b-col xl="4" md="6" >
                      <stats-card color="black" title="838293892382"
                                  sub-title="No. Rekening"
                      >
                      </stats-card>
                    </b-col>
                  <b-col xl="4" md="6" >
                      <stats-card color="black" title="13 Nov 2020"
                                  sub-title="Tanggal Request"
                      >
                      </stats-card>
                    </b-col>
                    <b-col xl="4" md="6" >
                      <stats-card color="black" title="09.00 WIB"
                                  sub-title="Jam Request"
                      >
                      </stats-card>
                    </b-col>
                  </b-row>
                  <b-row  style="margin-top:32px">
                    <b-col lg="12" class="pb-2 "><center><b-button size="sm" class="button-c1"><span>TOP UP</span></b-button></center></b-col>
                  </b-row>
                </b-tab>
              </b-tabs>
            </b-card>
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
