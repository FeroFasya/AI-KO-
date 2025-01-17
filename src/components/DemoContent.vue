<template>
  <section class="content">
    <div class="text-container">
      <h2>Upload Karya AI kamu !!!</h2>
      <p>Yuk, jelajahi karya AI yang super keren! Kamu juga bisa unggah karya kamu sendiri di sini. Siap-siap takjub, ya!</p>
      <a href="#faq" class="cta-button">Mau coba?</a>
    </div>
  </section>
</template>


<script>
export default {
  name: "DemoContent",
};
</script>

<style scoped>
.content {
  height: 100vh; /* Fullscreen height */
  display: flex;
  justify-content: center; /* Memposisikan konten di tengah secara horizontal */
  align-items: center; /* Memposisikan konten di tengah secara vertikal */
  background: linear-gradient(45deg, rgba(255, 0, 255, 0.5), rgba(0, 255, 255, 0.5)); /* Pink transparan */
  backdrop-filter: blur(3px); /* Blur background */
  color: white;
  padding: 0 20px;
  text-align: left; /* Set agar teks rata kiri */
}

.text-container {
  max-width: 600px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: flex-start; /* Teks di sebelah kiri */
  gap: 15px;
  z-index: 2; /* Pastikan konten tetap berada di atas latar belakang */
}

h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 10px;
}

p {
  font-size: 1rem;
  font-weight: 400;
  margin-bottom: 20px;
  line-height: 1.6;
  max-width: 480px; /* Lebar teks agar pas */
}

.cta-button {
  background-color: #ffffff;
  color: rgb(254, 126, 228);
  padding: 12px 25px;
  border-radius: 10px;
  font-weight: bold;
  text-decoration: none;
  font-size: 1.1rem;
  transition: background-color 0.3s;
}

.cta-button:hover {
  background-color: #e83e8c;
}

@media (max-width: 768px) {
  h2 {
    font-size: 1.8rem;
  }

  p {
    font-size: 0.9rem;
    max-width: 90%; /* Lebih luas pada layar kecil */
  }

  .cta-button {
    padding: 10px 20px;
  }
}
</style>
