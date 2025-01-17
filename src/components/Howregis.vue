<template>
    <section id="howregis" class="howregis-section">
      <div class="container">
        <h2>Cara Daftar & Login</h2>
  
        <p>Hai, teman-teman! Kami menyambut kalian untuk bergabung di website ini. Berikut cara yang bisa kalian pilih untuk memulai:</p>
  
        <div class="steps">
          <div class="step">
            <h3>1. Registrasi Akun</h3>
            <p>Untuk menggunakan semua fitur dari website ini, kalian perlu mendaftar terlebih dahulu. Kamu bisa klik tombol daftar dan ikuti langkah-langkahnya!</p>
          </div>
  
          <div class="step">
            <h3>2. Login dengan Google atau Discord</h3>
            <p>Login atau daftar lebih cepat dengan akun **Google** atau **Discord** kalian. Kami mendukung integrasi langsung supaya kamu bisa langsung masuk tanpa ribet!</p>
          </div>
  
          <div class="step">
            <h3>3. Akun Tamu (Guest)</h3>
            <p>Gak mau daftar? Tenang! Kalian tetap bisa menikmati beberapa fitur dengan membuat akun tamu. Akun tamu memungkinkan kalian untuk menjelajah dan mengupload karya tanpa memerlukan akun tetap.</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'HowRegis'
  }
  </script>
  
  <style scoped>
  .howregis-section {
    padding: 50px 0;
    background: linear-gradient(45deg, rgba(0, 255, 153, 0.7), rgba(0, 191, 255, 0.7)); /* Translucent background */
    text-align: center;
    color: #333;
  }
  
  h2 {
    font-size: 2rem;
    margin-bottom: 20px;
  }
  
  .steps {
    margin-top: 20px;
  }
  
  .step {
    background: linear-gradient(45deg, rgba(144, 255, 124, 0.8), rgba(0, 170, 255, 0.8));
    padding: 20px;
    margin: 10px;
    border-radius: 10px;
  }
  
  .step h3 {
    color: #ff4081; /* Pinkish */
  }
  </style>
  