<script>
export default {
  name: 'CaraKerja',
  data() {
    return {
      steps: [
        {
          number: 1,
          title: 'Daftarkan Bisnis Anda',
          description: 'Netizen, Restoran, supermarket, hotel, dan bisnis makanan lainnya dapat mendaftar sebagai donor makanan dalam platform kami.'
        },
        {
          number: 2,
          title: 'Laporkan Surplus Makanan',
          description: 'Donor dapat dengan mudah melaporkan surplus makanan mereka melalui aplikasi kami, menentukan jenis dan jumlah makanan yang tersedia.'
        },
        {
          number: 3,
          title: 'Koordinasi Pengambilan',
          description: 'Relawan kami akan mengkoordinasikan pengambilan dan pengiriman makanan ke organisasi sosial dan komunitas yang membutuhkan.'
        },
        {
          number: 4,
          title: 'Lacak Dampak Anda',
          description: 'Pantau dampak yang Anda buat dengan melihat data terperinci tentang kontribusi Anda terhadap pengurangan limbah makanan dan emisi karbon.'
        }
      ]
    }
  }
}
</script>

<template>
  <section class="how-it-works">
    <div class="container">
      <div class="section-title">
        <h2>Bagaimana Cara Kerjanya</h2>
        <p>Proses sederhana untuk menyelamatkan makanan dan membuat perbedaan</p>
      </div>
      <div class="steps-container">
        <div v-for="step in steps" :key="step.number" class="step">
          <div class="step-number">{{ step.number }}</div>
          <div class="step-content">
            <h3 class="step-title">{{ step.title }}</h3>
            <p class="step-description">{{ step.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>



<style scoped>
.how-it-works {
  padding: 80px 0;
  background-color: #f9f9f9;
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

.steps-container {
  display: flex;
  flex-direction: column;
  gap: 40px;
  margin-top: 40px;
}

.step {
  display: flex;
  align-items: center;
  gap: 40px;
}

.step-number {
  width: 60px;
  height: 60px;
  background-color: #27ae60;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  font-weight: 600;
  flex-shrink: 0;
}

.step-content {
  flex: 1;
}

.step-title {
  font-size: 1.4rem;
  margin-bottom: 10px;
  color: #333;
}

.step-description {
  color: #666;
  line-height: 1.6;
}

@media (max-width: 576px) {
  .step {
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
  }
}
</style>
