<template>
  <div id="app">
    <HeaderApp />
    <main>
      <DemoContent />
      <div class="section-divider"></div> <!-- Pemisah Section -->
      <RegisterForm />
      <div class="section-divider"></div> <!-- Pemisah Section -->
      <howregis />>
      <div class="section-divider"></div> <!-- Pemisah Section -->
      <Feature />
      <div class="section-divider"></div> <!-- Pemisah Section -->
      <Faq />
    </main>
    <FooterApp />
  </div>
</template>

<script>
import HeaderApp from './components/Header.vue';
import DemoContent from './components/DemoContent.vue';
import RegisterForm from './components/RegisterForm.vue';
import howregis from './components/Howregis.vue';
import Faq from './components/Faq.vue';
import FooterApp from './components/Footer.vue';
import Feature from './components/Feature.vue';



export default {
  name: 'App',
  components: {
    HeaderApp,
    DemoContent,
    RegisterForm,
    howregis,
    Feature,
    Faq,
    FooterApp,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');
html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  background: linear-gradient(to left, #272121, #000000);
  font-family: 'Poppins', sans-serif;
  color: white; /* Kontras dengan background gelap */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

/* Styling untuk pembatas antar section */
.section-divider {
  border-top: 2px solid #fff;  /* Garis putih */
  margin: 20px 0;              /* Memberikan jarak antar section */
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff; /* Sesuaikan agar teks tetap jelas */
  min-height: 100vh; /* Pastikan seluruh layar tercover */
  background: url('@/assets/bg.png') no-repeat center center fixed; 
  background-size: cover; /* Membuat gambar mencakup seluruh layar */
  margin: 0;
}

header, main, footer {
  max-width: 2000px;
  margin: 0 auto;
  padding: 90px;
  box-sizing: border-box;
}

/* Animasi smooth fade-in untuk halaman */
@keyframes fade-in {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

main {
  animation: fade-in 1s ease-in-out;
}

/* Responsive behavior */
@media (max-width: 768px) {
  header, main, footer {
    padding: 10px;
  }
}
</style>
