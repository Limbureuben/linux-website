<template>
  <section class="services-section">
    <!-- Header Banner -->
    <div class="services-header">
      <div class="container header-flex">
        <h2>Our Services</h2>
        <p>Empowering your digital future with secure, innovative, and scalable IT solutions</p>
      </div>
    </div>

    <div class="container services-content">
      <!-- Service 1: IT SUPPORT -->
      <div class="service-item animate-fade-up hover-lift">
        <div class="service-image">
          <img src="/image1.jpeg" alt="IT Support" />
        </div>
        <div class="service-text">
          <h3>IT SUPPORT</h3>
          <p>We offer fast, dependable and proactive assistance tailored to your needs include:</p>
          <ul>
            <li>System maintenance & health checks</li>
            <li>Troubleshooting & issue resolution</li>
            <li>Software installation & updates</li>
            <li>User support & training</li>
          </ul>
        </div>
      </div>

      <!-- Service 2: SYSTEM DEVELOPMENT -->
      <div class="service-item reverse animate-fade-up hover-lift" style="transition-delay: 0.1s">
        <div class="service-image">
          <img src="/image2.jpeg" alt="System Development" />
        </div>
        <div class="service-text">
          <h3>SYSTEM DEVELOPMENT</h3>
          <p>We design and build high-performance systems aligned with your business goals.</p>
          <ul>
            <li>Web & Mobile application development</li>
            <li>Custom software development</li>
            <li>Business process systems</li>
            <li>Database optimization</li>
          </ul>
        </div>
      </div>

      <!-- Service 3: CYBERSECURITY -->
      <div class="service-item animate-fade-up hover-lift" style="transition-delay: 0.2s">
        <div class="service-image">
          <img src="/image3.jpeg" alt="Cybersecurity" />
        </div>
        <div class="service-text">
          <h3>CYBERSECURITY</h3>
          <p>We safeguard your organization with advanced cybersecurity solutions include:</p>
          <ul>
            <li>Threat detection & prevention</li>
            <li>Firewall & encryption systems</li>
            <li>Security awareness training</li>
            <li>Vulnerability assessments</li>
          </ul>
        </div>
      </div>

      <!-- Service 4: AUTOMATION -->
      <div class="service-item reverse animate-fade-up hover-lift" style="transition-delay: 0.3s">
        <div class="service-image">
          <img src="/image4.jpeg" alt="Automation" />
        </div>
        <div class="service-text">
          <h3>AUTOMATION</h3>
          <p>We helps businesses embrace automation to save time, reduce manual work, and increase accuracy with intelligent tools</p>
          <ul>
            <li>Automated reporting systems</li>
            <li>Intelligent automation tools</li>
            <li>Business process optimization</li>
            <li>Workflow automation</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services-section {
  background-color: white;
  padding-bottom: 40px;
}

.container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 15px;
}

/* Header Banner */
.services-header {
  background-image: linear-gradient(to right, #004799, #002a5c); /* Blue gradient */
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

/* Add a subtle overlay or pattern if needed to match the "tech" look in the banner */
.services-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('/backgroundimage.jpeg'); /* Reusing background for texture */
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

.services-header h2 {
  font-size: 28px;
  font-weight: 700;
  margin: 0;
  white-space: nowrap;
}

.services-header p {
  font-size: 14px;
  opacity: 0.9;
  margin: 0;
  max-width: 500px;
}

/* Service Items */
.service-item {
  display: flex;
  align-items: center;
  gap: 40px;
  margin-bottom: 40px;
}

.service-item.reverse {
  flex-direction: row-reverse; /* For alternating layout */
}

.service-image {
  flex: 1;
}

.service-image img {
  width: 100%;
  border-radius: 4px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  height: 200px;
  object-fit: cover;
}

.service-text {
  flex: 1;
}

.service-text h3 {
  color: #000;
  font-size: 18px;
  font-weight: 700;
  margin-bottom: 10px;
  text-transform: uppercase;
}

.service-text p {
  color: #555;
  font-size: 14px;
  margin-bottom: 15px;
  line-height: 1.5;
}

.service-text ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.service-text ul li {
  position: relative;
  padding-left: 20px;
  margin-bottom: 8px;
  color: #555;
  font-size: 14px;
}

.service-text ul li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: #000; /* Black bullet */
  font-weight: bold;
}

/* Responsive */
@media (max-width: 768px) {
  .service-item {
    flex-direction: column;
    gap: 20px;
    margin-bottom: 40px;
  }
  
  .service-item.reverse {
    flex-direction: column;
  }
  
  .service-image img {
    height: auto;
    max-height: 200px;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .service-item {
    gap: 30px;
  }
  
  .service-image img {
    height: 180px;
  }
  
  .service-text h3 {
    font-size: 16px;
  }
  
  .service-text p, .service-text ul li {
    font-size: 13px;
  }
}
</style>
