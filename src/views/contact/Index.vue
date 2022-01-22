<template>
  <div class="contact">
    <Header />
    <header class="pt-5 border-bottom bg-light">
      <div class="container pt-md-1 pb-md-1">
        <h1 class="bd-title mt-5 font-weight-bold">
          <i class="fa fa-phone" aria-hidden="true"></i> KONTAK
        </h1>
        <p class="bd-lead">Kontak RSUD Kemayoran</p>
      </div>
    </header>

    <!-- Breadcrumb -->
    <nav aria-label="breadcrumb">
      <ol class="breadcrumb">
        <li class="breadcrumb-item">
          <router-link :to="{ name: 'home' }" class="text-decoration-none"
            ><i class="fa fa-home"></i> Home</router-link
          >
        </li>
        <li class="breadcrumb-item">
          <router-link :to="{ name: 'contact' }" class="text-decoration-none"
            ><i class="fa fa-phone"></i> Kontak</router-link
          >
        </li>
      </ol>
    </nav>
    <!-- End Breadcrumb -->

    <div class="container-fluid mt-3 mb-5">
      <div class="row">
        <div class="col-md-7">
          <div class="card border-0 shadow-sm rounded">
            <div class="card-body">
              <iframe
                src="https://maps.google.com/maps?ll=-6.1565127,106.8638865&q=RSUD Kemayoran&t=&z=14&ie=UTF8&iwloc=&output=embed"
                width="100%"
                height="400"
                frameborder="0"
                style="border: 0"
                allowfullscreen=""
                aria-hidden="false"
                tabindex="0"
              ></iframe>
            </div>
          </div>
        </div>
        <div class="col-md-5">
          <div class="card border-0 shadow-sm rounded">
            <div class="card-body">
              <h3>KONTAK KAMI</h3>
              <hr />
              <p>
                <i class="fa fa-map-marker" aria-hidden="true"></i> Jl. Serdang
                I No.3, RT.6/RW.5, Serdang, Kec. Kemayoran, Kota Jakarta Pusat,
                Daerah Khusus Ibukota Jakarta 10650
                <br />
                <i class="fas fa-phone"></i> (021) 4244277
                <br />
                <i class="fas fa-envelope"></i> rsukemayoran@gmail.com
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script>
//import component
import Header from "@/components/Header";
import Footer from "@/components/Footer";
export default {
  name: "ContactIndex",
  components: {
    Header,
    Footer,
  },
};
</script>
