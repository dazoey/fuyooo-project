<script>
export default {
  name: 'FiturSection',
  data() {
    return {
      features: [
        {
          icon: '🍽️',
          title: 'Selamatkan Makanan',
          description: 'Membantu bisnis makanan mengurangi limbah dan meningkatkan efisiensi dengan mendistribusikan kelebihan makanan mereka.'
        },
        {
          icon: '📱',
          title: 'Aplikasi Mudah',
          description: 'Platform yang mudah digunakan untuk menghubungkan donor makanan, relawan, dan penerima manfaat.'
        },
        {
          icon: '🌱',
          title: 'Dampak Lingkungan',
          description: 'Mengurangi emisi gas rumah kaca dengan mencegah makanan berakhir di tempat pembuangan sampah.'
        },
        {
          icon: '💵',
          title: 'Keuangan ',
          description: 'Sistem donasi dan dukungan finansial yang transparan untuk memastikan keberlanjutan operasional dan distribusi makanan'
        }
      ]
    }
  }
}
</script>

<template>
  <section class="features">
    <div class="container">
      <div class="section-title">
        <h2>Apa yang Kami Tawarkan</h2>
        <p>Platform terintegrasi yang menghubungkan semua pihak untuk menciptakan ekosistem makanan yang lebih berkelanjutan</p>
      </div>
      <div class="features-grid">
        <div v-for="(feature, index) in features" :key="index" class="feature-card">
          <div class="feature-icon">{{ feature.icon }}</div>
          <h3 class="feature-title">{{ feature.title }}</h3>
          <p class="feature-description">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>



<style scoped>
.features {
  padding: 80px 0;
  background-color: white;
}

.section-title {
  text-align: center;
  margin-bottom: 60px;
}

.section-title h2 {
  font-size: 2.2rem;
  color: #333;
  margin-bottom: 15px;
}

.section-title p {
  color: #666;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}

.feature-card {
  background-color: #f9f9f9;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.feature-icon {
  width: 70px;
  height: 70px;
  margin: 0 auto 20px;
  background-color: rgba(39, 174, 96, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  color: #27ae60;
}

.feature-title {
  font-size: 1.2rem;
  margin-bottom: 15px;
  color: #333;
}

.feature-description {
  color: #666;
  font-size: 0.95rem;
  line-height: 1.6;
}

@media (max-width: 992px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .features-grid {
    grid-template-columns: 1fr;
  }
}
</style>
