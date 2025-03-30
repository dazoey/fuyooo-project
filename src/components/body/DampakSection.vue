<script>
export default {
  name: 'DampakSection',
  data() {
    return {
      stats: [
        {
          number: '5.000+',
          text: 'Kilogram makanan diselamatkan'
        },
        {
          number: '120+',
          text: 'Bisnis makanan bergabung'
        },
        {
          number: '10.000+',
          text: 'Orang terbantu'
        }
      ]
    }
  }
}
</script>

<template>
  <section class="impact">
    <div class="container">
      <div class="section-title">
        <h2>Dampak yang Telah Kami Buat</h2>
        <p>Bersama-sama, kita membuat perbedaan yang nyata untuk lingkungan dan masyarakat</p>
      </div>
      <div class="impact-stats">
        <div v-for="(stat, index) in stats" :key="index" class="stat-card">
          <div class="stat-number">{{ stat.number }}</div>
          <p class="stat-text">{{ stat.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>



<style scoped>
.impact {
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

.impact-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  margin-top: 40px;
}

.stat-card {
  text-align: center;
  padding: 30px;
  background-color: #f9f9f9;
  border-radius: 10px;
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #27ae60;
  margin-bottom: 10px;
}

.stat-text {
  color: #666;
  font-size: 1rem;
}

@media (max-width: 768px) {
  .impact-stats {
    grid-template-columns: 1fr;
  }
}
</style>
