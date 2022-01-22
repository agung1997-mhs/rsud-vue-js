<template>
  <footer>
    <div class="container-fluid" style="background: white">
      <div class="row p-4">
        <div class="col-md-4">
          <h5>TENTANG</h5>
          <hr />
          <p>
            Rumah Sakit Umum Daerah Kemayoran merupakan rumah sakit pemerintah
            type D sesuai Keputusan Gubernur Nomor 1024 Tahun 2014 dengan
            kapasitas 29 tempat tidur yang awal mula berdiri pada tanggal 1
            April 2015. Rumah sakit ini merupakan pelimpahan yang dulunya adalah
            Puskesmas Kecamatan Kemayoran yang beralamat di Jl. Serdang Baru I
            Kelurahan Serdang Kecamatan Kemayoran Jakarta Pusat.
          </p>
        </div>
        <div class="col-md-4">
          <h5>TAGS</h5>
          <hr />
          <div v-if="tags.length > 0">
            <router-link
              :to="{ name: 'detail_tag', params: { slug: tag.slug } }"
              v-for="tag in tags"
              :key="tag.id"
              class="btn btn-sm btn-outline-secondary mb-2 me-2"
              >{{ tag.name.toUpperCase() }}</router-link
            >
          </div>
          <div v-else class="text-center">
            <ListLoader />
          </div>
        </div>
        <div class="col-md-4">
          <h5>KONTAK</h5>
          <hr />
          <p>
            <i class="fa fa-map-marker" aria-hidden="true"></i> Jl. Serdang I
            No.3, RT.6/RW.5, Serdang, Kec. Kemayoran, Kota Jakarta Pusat, Daerah
            Khusus Ibukota Jakarta <br />
            <i class="fas fa-phone"></i> 021 - 4244277
            <br />
            <i class="fas fa-envelope"></i> rsukemayoran@gmail.com
          </p>
        </div>
      </div>
    </div>
    <div class="container-fluid bg-dark">
      <div class="row p-3">
        <div class="text-center text-white font-weight-bold">
          Copyright © 2022 RSUD KEMAYORAN. All rights reserved.
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
// import content loader
import { ListLoader } from "vue-content-loader";
// import axios
import axios from "axios";
export default {
  name: "Footer",
  components: {
    // loader component
    ListLoader,
  },
  data() {
    return {
      tags: [],
    };
  },
  created() {
    axios.get("/api/tag").then((response) => {
      this.tags = response.data.data.data;
    });
  },
};
</script>
