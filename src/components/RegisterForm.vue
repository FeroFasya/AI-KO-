<template>
  <section class="register">
    <h2>Daftar atau Login</h2>
    <p>Yuk, daftar dulu biar bisa akses fitur website ini sepenuhnya!</p>
    <form @submit.prevent="handleRegister">
      <input type="text" v-model="name" placeholder="Nama Lengkap" required />
      <input type="email" v-model="email" placeholder="Email" required />
      <input
        type="tel"
        v-model="phone"
        placeholder="Nomor Telepon (Opsional)"
        pattern="\\+?[0-9]{8,15}"
      />
      <button type="submit" class="primary-btn">Daftar</button>
    </form>

    <div class="alternative-login">
      <p>Atau masuk dengan:</p>
      <div class="social-buttons">
        <button @click="handleGoogleLogin" class="social-btn google-btn">
          <img src="@/assets/google.png" alt="Google" />
        
        </button>
        <button @click="handleDiscordLogin" class="social-btn discord-btn">
          <img src="@/assets/discord.png" alt="Discord" />
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "RegisterForm",
  data() {
    return {
      name: "",
      email: "",
      phone: "",
    };
  },
  methods: {
    handleRegister() {
      alert(`Terima kasih, ${this.name}! Pendaftaranmu berhasil.`);
    },
    handleGoogleLogin() {
      alert("Mengarahkan ke login Google...");
      // Tambahkan logika redirect ke Google
    },
    handleDiscordLogin() {
      alert("Mengarahkan ke login Discord...");
      // Tambahkan logika redirect ke Discord
    },
  },
};
</script>

<style scoped>
.register {
  max-width: 2000px;
  margin: auto;
  padding: 20px;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  text-align: center;
}

h2 {
  color: #ff69b4;
  font-size: 1.8rem;
  margin-bottom: 10px;
}

p {
  color: #555;
  font-size: 1rem;
  margin-bottom: 20px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

input {
  width: 100%;
  padding: 10px;
  font-size: 1rem;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.primary-btn {
  padding: 12px;
  font-size: 1.2rem;
  background: #ff69b4;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
}

.primary-btn:hover {
  background: #ff8ebc;
}

.alternative-login {
  margin-top: 20px;
}

p {
  margin-bottom: 15px;
}

.social-buttons {
  display: flex;
  gap: 10px;
  justify-content: center;
}

.social-btn {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px 15px;
  background: #f5f5f5;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.3s;
}

.social-btn img {
  width: 20px;
  height: 20px;
}

.google-btn:hover {
  background: #e5e5e5;
}

.discord-btn:hover {
  background: #ebebeb;
}
</style>
