<template>
  <section class="mission-vision-section">
    <div class="container">
      <h2 class="section-title">Our mission and vision</h2>
      <div class="mission-vision-grid">
        <!-- Mission Card -->
        <div class="mv-card animate-slide-left">
          <div class="mv-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#004799" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2L2 7l10 5 10-5-10-5z"></path><path d="M2 17l10 5 10-5"></path><path d="M2 12l10 5 10-5"></path></svg>
          </div>
          <div class="mv-content">
            <h3>Our Mission</h3>
            <p>To empower businesses through innovative IT solutions, ensuring security, efficiency, and growth. We are dedicated to providing cutting-edge technology that transforms operations and drives sustainable success for our clients.</p>
          </div>
        </div>

        <!-- Vision Card -->
        <div class="mv-card animate-slide-right" style="transition-delay: 0.2s">
          <div class="mv-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#34BB78" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"></circle><line x1="2" y1="12" x2="22" y2="12"></line><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"></path></svg>
          </div>
          <div class="mv-content">
            <h3>Our Vision</h3>
            <p>To be the leading provider of transformative technology services, shaping a digital future for all. We strive to be at the forefront of technological advancement, creating a world where innovation is accessible and impactful.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.mission-vision-section {
  padding: 60px 0 80px;
  background-color: #F8FAFC;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 15px;
}

.section-title {
  font-size: 32px;
  font-weight: 700;
  color: #004799;
  margin-bottom: 40px;
  text-align: center;
}

/* Grid and Cards */
.mission-vision-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
}

.mv-card {
  background: white;
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  transition: transform 0.3s ease;
}

.mv-card:hover {
  transform: translateY(-5px);
}

.mv-icon {
  background: #f0f7ff;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 25px;
}

.mv-card:nth-child(2) .mv-icon {
  background: #f0fff4;
}

.mv-content h3 {
  font-size: 24px;
  font-weight: 700;
  color: #004799;
  margin-bottom: 15px;
}

.mv-card:nth-child(2) .mv-content h3 {
  color: #34BB78;
}

.mv-content p {
  font-size: 16px;
  color: #4A5568;
  line-height: 1.7;
  margin: 0;
}

/* Responsive */
@media (max-width: 768px) {
  .mission-vision-grid {
    grid-template-columns: 1fr;
  }
  
  .header-flex {
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
  }
  
  .mission-vision-header h2 {
    font-size: 24px;
  }
  
  .mv-card {
    padding: 30px;
  }
}
</style>
