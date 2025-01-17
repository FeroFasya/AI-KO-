<template>
  <section id="features" class="features-section">
    <h2>Fitur Web Ini & Panduan Penggunaannya</h2>

    <div class="feature-item">
      <img src="/assets/profil-page.png" alt="Halaman Profil" class="feature-image" />
      <h3>Halaman Profil</h3>
      <p>Setelah kamu login atau registrasi, kamu bisa mengakses halaman profil. Di sini, kamu bisa lihat info kamu dan edit profil sesuai keinginan. Seru kan?</p>
    </div>

    <div class="feature-item">
      <img src="/assets/jelajah-page.png" alt="Halaman Jelajah" class="feature-image" />
      <h3>Halaman Jelajah</h3>
      <p>Kalau kamu penasaran dengan karya-karya AI lainnya, kamu bisa masuk ke halaman Jelajah. Di sana, kamu bisa lihat karya dari user lain yang udah diupload dan cari inspirasi seru!</p>
    </div>

    <div class="feature-item">
      <img src="/assets/upload-page.png" alt="Halaman Upload" class="feature-image" />
      <h3>Halaman Upload</h3>
      <p>Kalau kamu mau berbagi karya kamu, halaman Upload adalah tempat yang tepat! Cukup klik tombol upload, pilih karya, dan tunggu karya kamu tampil di situs.</p>
    </div>

    <div class="feature-item">
      <img src="@/assets/bg.png" alt="Halaman Follow" class="feature-image" />
      <h3>Halaman Follow & Komunitas</h3>
      <p>Jangan lupa follow creator yang kamu suka, biar gak ketinggalan karya-karya keren mereka. Bikin juga komunitas kecilmu sendiri, biar makin asik ngobrol seputar karya!</p>
    </div>

    <div class="feature-item">
      <img src="/assets/chat-page.png" alt="Halaman Chat" class="feature-image" />
      <h3>Halaman Chat (Direct Message)</h3>
      <p>Kalau kamu mau ngobrol langsung sama sesama pengguna, halaman Chat bisa jadi tempat yang tepat. Cuma kamu dan lawan bicaramu yang bisa lihat percakapan kalian, jadi nyaman buat ngirim pesan!</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "FeatureApp",
}
</script>

<style scoped>
.features-section {
  background-color: rgba(0, 0, 0, 0.5); /* Semi transparan biar background keliatan */
  color: #fff;
  padding: 50px;
  margin-top: 50px;
  text-align: center;
}

.feature-item {
  margin-bottom: 30px;
  text-align: left;
}

.feature-item img {
  width: 100%; 
  max-width: 600px;
  height: 300px;         /* Ukuran tinggi gambar bisa disesuaikan */
  object-fit: cover;     /* Mengisi container secara penuh tanpa merusak aspect ratio */
  border-radius: 10px;
  margin-bottom: 15px;
}

.feature-item h3 {
  font-size: 1.5rem;
  margin-bottom: 10px;
  text-align: left;
}

.feature-item p {
  font-size: 1.1rem;
  line-height: 1.6;
}
</style>
