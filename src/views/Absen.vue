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
          <h3 class="mb-0" style="color:black;font-size:16px;margin-bottom:24px !important;font-weight:500">Absensi</h3>
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
      </b-row>
      <b-row>
        
      </b-row>
        <b-row style="margin-top:55px">
          <b-col>
           
                  <b-card no-body style="border:none !important">
       
        <el-table class="table-responsive table"
                  header-row-class-name="thead-light"
                  :data="projects">
            <el-table-column label="Code"
                             min-width="110px"
                             prop="code">
                <template v-slot="{row}">
                    <b-media no-body class="align-items-center">
                        
                        <b-media-body>
                            <span style="font-size:12px;" class="font-weight-400 name mb-0 text-sm">{{row.code}}</span>
                        </b-media-body>
                    </b-media>
                </template>
            </el-table-column>
            <el-table-column label="Driver"
                             min-width="110px"
                             prop="driver">
                <template v-slot="{row}">
                    <b-media no-body class="align-items-center">
                        
                        <b-media-body>
                            <span style="font-size:12px;" class="font-weight-400 name mb-0 text-sm">{{row.driver}}</span>
                        </b-media-body>
                    </b-media>
                </template>
            </el-table-column>
            <el-table-column label="Jam Siap"
                             min-width="110px"
                             prop="jamSiap">
                <template v-slot="{row}">
                    <b-media no-body class="align-items-center">
                        
                        <b-media-body>
                            <span style="font-size:12px;" class="font-weight-400 name mb-0 text-sm">{{row.jamSiap}}</span>
                        </b-media-body>
                    </b-media>
                </template>
            </el-table-column>
            
            <el-table-column label="Jam Masuk"
                             min-width="110px"
                             prop="jamMasuk">
                <template v-slot="{row}">
                    <b-media no-body class="align-items-center">
                        
                        <b-media-body>
                            <span style="font-size:12px;color:#F8B551" class="font-weight-400 name mb-0 text-sm">{{row.jamMasuk}}</span>
                        </b-media-body>
                    </b-media>
                </template>
            </el-table-column>
            <el-table-column label="Jam Pulang"
                             min-width="110px"
                             prop="jamMasuk">
                <template v-slot="{row}">
                    <b-media no-body class="align-items-center">
                        
                        <b-media-body>
                            <span style="font-size:12px;color:#59D185" class="font-weight-400 name mb-0 text-sm">{{row.jamMasuk}}</span>
                        </b-media-body>
                    </b-media>
                </template>
            </el-table-column>
            <el-table-column label="Siklus Tgl"
                             min-width="110px"
                             prop="siklusTanggal">
                <template v-slot="{row}">
                    <b-media no-body class="align-items-center">
                        
                        <b-media-body>
                            <span style="font-size:12px;" class="font-weight-400 name mb-0 text-sm">{{row.siklusTanggal}}</span>
                        </b-media-body>
                    </b-media>
                </template>
            </el-table-column>
           
        </el-table>

        
    </b-card>
            
          </b-col>
        </b-row>
      
    </b-container>

  </div>
</template>
<script>
  // Charts
  import * as chartConfigs from '@/components/Charts/config';
 
  import { Carousel, Slide } from 'vue-carousel';

  // Components
  import StatsCard from '@/components/Cards/StatsCard';

  // Tables
  import projects from './Tables/projects'
  import SocialTrafficTable from './Dashboard/SocialTrafficTable';
  import PageVisitsTable from './Dashboard/PageVisitsTable';
    import { Table, TableColumn} from 'element-ui'

  export default {
    components: {
      
      StatsCard,
      PageVisitsTable,
      SocialTrafficTable,
      Carousel,
      Slide,
      [Table.name]: Table,
      [TableColumn.name]: TableColumn
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
        },
        projects,
        currentPage: 1
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
