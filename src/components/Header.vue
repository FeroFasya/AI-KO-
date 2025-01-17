<template>
  <header>
    <div class="header-container">
      <h1 class="logo">AI KO!</h1>
      <nav>
        <ul :class="['nav-links', isMenuOpen ? 'show' : '']">
          <li><a href="#home" @click="closeMenu">Home</a></li>
          <li><a href="#features" @click="closeMenu">Features</a></li>
          <li><a href="#howregis" @click="closeMenu">How</a></li>
          <li><a href="#faq" @click="closeMenu">FAQ</a></li>
        </ul>
        <!-- Tombol CTA di sebelah kanan -->
        <a href="#register" class="cta-button">Regis Yuk!</a>
        <button class="menu-toggle" @click="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </button>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderApp",
  data() {
    return {
      isMenuOpen: false,
    };
  },
  mounted() {
    // Menambahkan event listener saat komponen di-mount
    window.addEventListener("click", this.closeMenuOnClickOutside);
  },
  beforeUnmount() {
    // kode sebelum komponen dihancurkan
    window.removeEventListener("click", this.closeMenuOnClickOutside);
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false; // Menutup menu setelah item diklik
    },
    closeMenuOnClickOutside(event) {
      // Cek jika klik terjadi di luar menu
      if (this.$el && !this.$el.contains(event.target)) {
        this.closeMenu();
      }
    }
  },
};
</script>

<style scoped>
/* Header styling */
header {
  background: rgba(51, 51, 51, 0.8); /* Semi-transparan untuk efek elegan */
  color: #fff;
  padding: 8px 20px;
  position: sticky;
  top: 0;
  z-index: 1000;
  backdrop-filter: blur(0px); /* Blur effect di belakang header */
  width: 100%;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

/* Header Container */
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 10px;
}

/* Logo */
.logo {
  font-size: 1.5rem; /* Ukuran lebih kecil untuk tampilan minimal */
  font-weight: 600;
  color: #ffc0cb; /* Soft pink untuk keunikan */
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
}

/* Navigation styling */
nav {
  display: flex;
  align-items: center;
}

.nav-links {
  display: flex;
  gap: 15px;
  list-style: none;
  transition: transform 0.3s;
}

.nav-links a {
  text-decoration: none;
  color: white;
  font-weight: 500;
  font-size: 0.9rem; /* Ukuran font kecil untuk elegan */
  transition: color 0.2s ease, border-bottom 0.3s ease;
  border-bottom: 2px solid transparent;
}

.nav-links a:hover {
  color: #ffc0cb; /* Pink ketika hover */
  border-bottom: 2px solid #ffc0cb;
}

/* CTA Button */
.cta-button {
  padding: 10px 20px;
  background-color: #ff69b4;
  color: white;
  font-size: 1.0rem;
  text-decoration: none;
  border-radius: 10px;
  font-weight: bold;
  margin-left: 20px;
  transition: background-color 0.3s;
}

.cta-button:hover {
  background-color: #e60b8b;
}

/* Animasi Glow pada Logo */
@keyframes glow {
  from {
    text-shadow: 0 0 10px #ff69b4, 0 0 20px #ff69b4, 0 0 30px #ff69b4;
  }
  to {
    text-shadow: 0 0 20px #fff, 0 0 30px #ff69b4, 0 0 40px #ff69b4;
  }
}

/* Responsive Menu */
.menu-toggle {
  display: none;
  flex-direction: column;
  gap: 4px;
  background: none;
  border: none;
  cursor: pointer;
}

.menu-toggle span {
  display: block;
  width: 25px;
  height: 3px;
  background-color: white;
  border-radius: 3px;
  transition: transform 0.3s, background-color 0.3s;
}

/* When Menu is Open */
.nav-links.show {
  position: absolute;
  top: 60px;
  right: 0;
  background-color: rgba(51, 51, 51, 0.95);
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
  flex-direction: column;
  align-items: flex-start;
  width: 80%;
  max-width: 300px;
  padding: 15px;
  gap: 10px;
  border-radius: 8px;
}

/* Responsive for Mobile */
@media (max-width: 768px) {
  .menu-toggle {
    display: flex;
  }

  .nav-links {
    display: none;
  }

  .nav-links.show {
    display: flex;
  }

  /* Pastikan tombol CTA tetap di kanan */
  .cta-button {
    display: none;
  }
}
</style>
