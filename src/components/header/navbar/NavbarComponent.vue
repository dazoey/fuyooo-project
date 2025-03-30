<script>
export default {
  name: 'NavbarComponent',
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    scrollToHow() {
      const FuuuyoSection = document.getElementById('CaraKerja-section');
      if (FuuuyoSection) {
        FuuuyoSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToAbout() {
      const FuuuyoSection = document.getElementById('About-section');
      if (FuuuyoSection) {
        FuuuyoSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    goToCharity() {
      this.$router.push('/charity');
    }
  }
}
</script>
<template>
  <nav class="navbar">
    <div class="container navbar-container">
      <router-link to="/" class="logo">Fu<span>Yooo</span></router-link>
      <ul class="nav-menu" :class="{ 'active': isMenuOpen }">
        <li><router-link to="/homeview">Beranda</router-link></li>
        <li><a @click="scrollToAbout">Tentang Kami</a></li>
        <li><a @click="scrollToHow">Cara Kerja</a></li>
        <li><a @click="scrollToAbout">Kontak</a></li>
      </ul>
      <router-link to="/charity" class="nav-btn">Mulai Sekarang</router-link>
      <div class="hamburger" @click="toggleMenu">☰</div>
    </div>
  </nav>
</template>



<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: white;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  padding: 15px 0;
}

.navbar-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.8rem;
  font-weight: 700;
  color: #27ae60;
  text-decoration: none;
}

.logo span {
  color: #f39c12;
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 30px;
}

.nav-menu li a {
  text-decoration: none;
  color: #555;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-menu li a:hover {
  color: #27ae60;
}

.nav-btn {
  background-color: #27ae60;
  color: white;
  padding: 10px 20px;
  border-radius: 30px;
  font-weight: 500;
  text-decoration: none;
  transition: background-color 0.3s ease;
}

.nav-btn:hover {
  background-color: #219653;
}

.hamburger {
  display: none;
  cursor: pointer;
}

@media (max-width: 768px) {
  .nav-menu {
    position: fixed;
    top: 70px;
    right: -100%;
    flex-direction: column;
    background-color: white;
    width: 100%;
    text-align: center;
    transition: 0,8s;
    box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
    padding: 20px 0;
    gap: 15px;
  }

  .nav-menu.active {
    left: 0;
  }

  .hamburger {
    display: block;
  }
}
</style>
