<template>
  <section class="projects-section">
    <!-- Header Banner -->
    <div class="projects-header">
      <div class="container header-flex">
        <h2>Our Successful Projects</h2>
        <p>Discover our portfolio of successful projects built to solve real-world business challenges through technology</p>
      </div>
    </div>

    <div class="container">
      <!-- Filter Bar -->
      <div class="filter-bar">
        <button 
          v-for="filter in filters" 
          :key="filter"
          :class="['filter-btn', { active: activeFilter === filter }]"
          @click="activeFilter = filter"
        >
          {{ filter }}
        </button>
      </div>

      <!-- Projects Grid/Carousel -->
      <div class="projects-container">
        <button class="nav-btn prev">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="15 18 9 12 15 6"></polyline></svg>
        </button>

        <div class="projects-grid">
          <div 
            v-for="(project, index) in filteredProjects" 
            :key="project.id" 
            class="project-card animate-fade-up hover-lift"
            :style="{ transitionDelay: (index * 0.1) + 's' }"
          >
            <div class="project-image">
              <img :src="project.image" :alt="project.title" />
              <div class="play-icon">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="white"><path d="M8 5v14l11-7z"></path></svg>
              </div>
            </div>
            <div class="project-info">
              <span class="category-tag">{{ project.category }}</span>
              <h3>{{ project.title }}</h3>
              <a href="#" class="case-study-link">
                View Case Study
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="9 18 15 12 9 6"></polyline></svg>
              </a>
            </div>
          </div>
        </div>

        <button class="nav-btn next">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="9 18 15 12 9 6"></polyline></svg>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from 'vue'

const filters = ['All projects', 'System Development', 'Cybersecurity', 'Automation']
const activeFilter = ref('All projects')

const projects = [
  {
    id: 1,
    title: 'E-commerce Platform Revamp',
    category: 'System Development',
    image: '/image1.jpeg'
  },
  {
    id: 2,
    title: 'Secure Shield Cyber Defense',
    category: 'Cybersecurity',
    image: '/image2.jpeg'
  },
  {
    id: 3,
    title: 'Automated Workflow solutions',
    category: 'Automation',
    image: '/image3.jpeg'
  }
]

const filteredProjects = computed(() => {
  if (activeFilter.value === 'All projects') return projects
  return projects.filter(p => p.category === activeFilter.value)
})
</script>

<style scoped>
.projects-section {
  padding-bottom: 80px;
  background-color: white;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 15px;
}

/* Header Banner */
.projects-header {
  background-image: linear-gradient(to right, #004799, #002a5c);
  color: white;
  padding: 20px 0;
  margin-bottom: 40px;
  position: relative;
  overflow: hidden;
  max-width: 1100px;
  margin-left: auto;
  margin-right: auto;
  border-radius: 0;
}

.projects-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('/backgroundimage.jpeg');
  opacity: 0.1;
  background-size: cover;
}

.header-flex {
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;
}

.projects-header h2 {
  font-size: 28px;
  font-weight: 700;
  margin: 0;
  white-space: nowrap;
}

.projects-header p {
  font-size: 14px;
  opacity: 0.9;
  margin: 0;
  max-width: 500px;
}

/* Filter Bar */
.filter-bar {
  display: flex;
  gap: 15px;
  margin-bottom: 40px;
  justify-content: flex-start;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 10px 20px;
  border: none;
  border-radius: 6px;
  background-color: #E2E8F0;
  color: #333;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s;
}

.filter-btn.active {
  background-color: #004799;
  color: white;
}

/* Projects Container */
.projects-container {
  display: flex;
  align-items: center;
  gap: 20px;
  position: relative;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 25px;
  flex: 1;
}

.project-card {
  background: #F8FAFC;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  transition: transform 0.3s;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-image {
  position: relative;
  height: 200px;
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.play-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: rgba(255, 255, 255, 0.2);
  border: 2px solid white;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  backdrop-filter: blur(4px);
}

.project-info {
  padding: 20px;
}

.category-tag {
  display: inline-block;
  background-color: #004799;
  color: white;
  font-size: 11px;
  padding: 4px 12px;
  border-radius: 4px;
  margin-bottom: 12px;
  text-transform: capitalize;
}

.project-info h3 {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 15px;
  color: #1A202C;
}

.case-study-link {
  display: flex;
  align-items: center;
  gap: 5px;
  color: #004799;
  text-decoration: none;
  font-size: 14px;
  font-weight: 500;
}

.nav-btn {
  background: none;
  border: none;
  color: #CBD5E0;
  cursor: pointer;
  padding: 10px;
  transition: color 0.3s;
}

.nav-btn:hover {
  color: #004799;
}

/* Responsive */
@media (max-width: 992px) {
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
  
  .nav-btn {
    display: none;
  }
  
  .projects-header h2 {
    font-size: 24px;
  }
}
</style>
