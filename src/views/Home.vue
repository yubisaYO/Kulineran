<template>
  <div class="home bg-success-subtle">
    <NavBar />
    <div class="container">
      <Hero />
      <div class="row">
        <div class="col">
          <h2>Best <strong>Foods</strong></h2>
        </div>
        <div class="col">
          <router-link to="/foods" class="btn btn-success float-right">
            <b-icon-eye class="mr-2"></b-icon-eye>Lihat Semua</router-link
          >
        </div>
      </div>

      <div class="row">
        <div
          class="col-md-3 mt-4"
          v-for="product in products"
          :key="product.id"
        >
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "HomeView", //harus multi-word
  components: {
    NavBar,
    Hero,
    CardProduct,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/best-products")
      .then((response) => {
        this.setProduct(response.data);
      })
      .catch((error) => {
        // handle error
        console.log(error);
      });
  },
};
</script>
