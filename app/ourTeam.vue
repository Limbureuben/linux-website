<template>
  <section class="our-team-section">
    <div class="container">
      <h2 class="section-title">Meet Our Team</h2>
      <div class="team-grid">
        <div v-for="(member, index) in team" :key="member.id" 
             class="team-card animate-fade-up hover-lift"
             :style="{ transitionDelay: (index * 0.1) + 's' }">
          <div class="member-image">
            <img :src="member.image" :alt="member.name" />
            <div class="social-overlay">
              <a href="#" class="social-link"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg></a>
              <a href="#" class="social-link"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path></svg></a>
            </div>
          </div>
          <div class="member-info">
            <h3>{{ member.name }}</h3>
            <p>{{ member.role }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const team = [
  { id: 1, name: 'Allan Fernandez', role: 'Founder', image: '/profile.jpeg' },
  { id: 2, name: 'Reuben Limbu', role: 'CEO', image: '/profile.jpeg' },
  { id: 3, name: 'Robert Wilson', role: 'Project Manager', image: '/profile.jpeg' },
  { id: 4, name: 'Sarah Johnson', role: 'Lead Developer', image: '/profile.jpeg' }
]
</script>

<style scoped>
.our-team-section {
  padding: 80px 0;
  background-color: white;
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
  margin-bottom: 50px;
  text-align: center;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 30px;
}

.team-card {
  text-align: center;
  transition: transform 0.3s ease;
}

.team-card:hover {
  transform: translateY(-10px);
}

.member-image {
  position: relative;
  width: 100%;
  aspect-ratio: 1 / 1;
  border-radius: 12px;
  overflow: hidden;
  margin-bottom: 20px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.05);
}

.member-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.social-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 71, 153, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.team-card:hover .social-overlay {
  opacity: 1;
}

.social-link {
  color: white;
  background: rgba(255, 255, 255, 0.2);
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background 0.3s ease;
}

.social-link:hover {
  background: white;
  color: #004799;
}

.member-info h3 {
  font-size: 20px;
  font-weight: 700;
  color: #1A202C;
  margin-bottom: 5px;
}

.member-info p {
  font-size: 14px;
  color: #34BB78;
  font-weight: 500;
  margin: 0;
}

/* Responsive */
@media (max-width: 992px) {
  .team-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .team-grid {
    grid-template-columns: 1fr;
    max-width: 300px;
    margin: 0 auto;
  }
}
</style>
