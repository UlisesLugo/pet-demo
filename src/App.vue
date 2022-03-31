<script>
import NavBar from "./components/NavBar.vue";
export default {
  name: "App",
  components: {
    NavBar,
  },
  data() {
    return {
      message: "Hello World!",
      images: [
        "https://parade.com/wp-content/uploads/2019/04/pet-quotes.jpg",
        "https://i.imgur.com/rmydi2w.jpg",
        "http://yourdost-blog-images.s3-ap-southeast-1.amazonaws.com/wp-content/uploads/2016/01/03165939/Dogs.jpg",
      ],
      currentImage: 0,
    };
  },
  methods: {
    nextImage() {
      this.currentImage += 1;
      if (this.currentImage == this.images.length) {
        this.currentImage = 0;
      }
    },
  },
};
</script>

<template>
  <v-app>
    <NavBar />
    <v-main>
      <img
        alt="Vue logo"
        class="logo"
        :src="images[currentImage]"
        width="250"
        height="250"
      />
      <v-btn @click="nextImage">Cambiar imagen</v-btn>
      <h1 class="green">El mundo de las mascotas</h1>
    </v-main>
  </v-app>
</template>

<style>
#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
}
</style>
