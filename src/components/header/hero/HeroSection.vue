<script>
export default {
  name: 'HeroSection',
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    scrollToFitur() {
      const FuuuyoSection = document.getElementById('Fitur-section');
      if (FuuuyoSection) {
        FuuuyoSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
  }
}


</script>

<template>
  <section class="hero">
    <div class="container hero-container">
      <div class="hero-content">
        <h1 class="hero-title">Solusi Makanan <span>Berkelanjutan</span> untuk Indonesia</h1>
        <p class="hero-description">Kami menghubungkan surplus makanan dari restoran dan supermarket bahkan Netizen dengan mereka yang membutuhkan, mengurangi limbah makanan dan memerangi kelaparan dalam satu langkah.</p>
        <div class="hero-buttons">
          <a href="/charity" class="primary-btn">Mulai Sekarang</a>
          <a href="#" @click="scrollToFitur" class="secondary-btn">Pelajari Lebih Lanjut</a>
        </div>
      </div>
      <div class="hero-image">
        <img src="https://imgur.com/nlRr5vn.jpg" alt="Food Rescue">
      </div>
    </div>
  </section>
</template>



<style scoped>
.hero {
  padding-top: 120px;
  padding-bottom: 80px;
  background-color: #f9f9f9;
}

.hero-container {
  display: flex;
  align-items: center;
  gap: 50px;
}

.hero-content {
  flex: 1;
}

.hero-title {
  font-size: 2.8rem;
  font-weight: 700;
  margin-bottom: 20px;
  color: #333;
  line-height: 1.2;
}

.hero-title span {
  color: #27ae60;
}

.hero-description {
  font-size: 1.1rem;
  color: #666;
  margin-bottom: 30px;
  line-height: 1.6;
}

.hero-buttons {
  display: flex;
  gap: 15px;
}

.primary-btn {
  background-color: #27ae60;
  color: white;
  padding: 12px 25px;
  border-radius: 30px;
  font-weight: 500;
  text-decoration: none;
  transition: background-color 0.3s ease;
}

.primary-btn:hover {
  background-color: #219653;
}

.secondary-btn {
  background-color: white;
  color: #27ae60;
  padding: 12px 25px;
  border-radius: 30px;
  font-weight: 500;
  text-decoration: none;
  border: 2px solid #27ae60;
  transition: all 0.3s ease;
}

.secondary-btn:hover {
  background-color: #27ae60;
  color: white;
}

.hero-image {
  flex: 1;
  text-align: center;
}

.hero-image img {
  max-width: 100%;
  border-radius: 10px;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .hero-container {
    flex-direction: column;
  }
  .hero-image {
    order: -1;
  }
}

@media (max-width: 576px) {
  .hero-buttons {
    flex-direction: column;
  }
}
</style>
