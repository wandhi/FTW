<template>
 <b-row style="display:flex;justify-content:flex-start;align-items:center;max-width:550px;margin-top:13px">
       <b-col cols="2">
         <b-img src="img/brand/prof.png" style="width:48px;height:48px;border-radius:59px" fluid alt="Responsive image"></b-img>
       </b-col>
       <b-col cols="10">
        <b-row>
          <b-col cols="2">
            <span style="font-weight:400;font-size:10px;color:#A8A8A8" v-if="code">{{code}}</span>
          </b-col>
          <b-col cols="10" class="flex-row" style="justify-content:flex-end">
              <span style="font-weight:400;font-size:10px;color:#333335" v-if="time && date">{{time}} • {{date}}</span>
            
          </b-col>
        </b-row>
        <b-row>
          <b-col cols=12>
            <span style="font-weight:500;font-size:14px;color:#333335" v-if="code && driver">{{code}} || {{driver}}</span>
          </b-col>
        </b-row>
        <b-row>
          <b-col cols=12>
            <span v-if="type=='pengeluaran'" style="font-weight:400;font-size:14px;color:#333335">Melakukan pengeluaran <b v-if="pengeluaran">{{pengeluaran}}</b> sebesar <span v-if="total" style="color:#FD8C8C;font-weight:500">{{total}}</span></span>
            <span v-if="type=='absen'" style="font-weight:400;font-size:14px;color:#333335">Melakukan <span v-if="absenMasuk" style="color:#59D185"> Absen masuk </span>pada <span v-if="absenMasuk" style="font-weight:600">{{absenMasuk}}</span></span><br v-if="absenMasuk">
            <span v-if="type=='absen'" style="font-weight:400;font-size:14px;color:#333335">Melakukan <span v-if="absenPulang" style="color:#FFAD57"> Absen Pulang </span>pada <span v-if="absenPulang" style="font-weight:600">{{absenPulang}}</span></span>
            <span v-if="type=='izin'" style="font-weight:400;font-size:14px;color:#333335"><span v-if="tanggalIzin" style="color:#FFAD57"> Izin tidak masuk </span>pada tanggal<span v-if="tanggalIzin" style="font-weight:600">{{tanggalIzin}}</span></span>
            <span v-if="type=='libur'" style="font-weight:400;font-size:14px;color:#333335"><span v-if="tanggalLibur" style="color:#FD8C8C"> Libur tidak masuk </span>pada tanggal<span v-if="tanggalLibur" style="font-weight:600"> {{tanggalLibur}}</span></span>

          </b-col>
        </b-row>
       </b-col>
      </b-row>
</template>
<script>
  import Card from './Card.vue';

  export default {
    name: 'notif-card',
    components: {
      Card
    },
    props: {
      icon: String,
      code: String,
      driver: String,
      time: String,
      date: String,
      type: String,
      pengeluaran: String,
      total: String,
      absenMasuk: String,
      absenPulang: String,
      tanggalIzin: String,
      tanggalLibur: String,
      tanggalRevisi: String

    }
  };
</script>
<style></style>
