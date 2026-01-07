<template>
  <section class="about-us-section">
    <div class="container about-content">
      <!-- Left Column: Images -->
      <div class="image-grid animate-slide-left">
        <div class="image-col-1">
          <img src="/image1.jpeg" alt="Team meeting" class="about-img img-1" />
          <img src="/image3.jpeg" alt="Coding" class="about-img img-3" />
        </div>
        <div class="image-col-2">
          <img src="/image2.jpeg" alt="Developer working" class="about-img img-2" />
          <img src="/image4.jpeg" alt="Office work" class="about-img img-4" />
        </div>
      </div>

      <!-- Right Column: Text -->
      <div class="text-content animate-slide-right" style="transition-delay: 0.2s">
        <div class="section-header">
          <h2>ABOUT US</h2>
        </div>
        <h3>Empowering your technology journey</h3>
        <p class="description">
          At Lanix technologies, we dedicate to empowering businesses through innovative IT solutions. From reliable IT support to cutting-edge system development, robust cybersecurity, and intelligent automation, we provide comprehensive services designed to optimize performance and safeguard your operations. Our team of experts combines technical expertise with forward a forward-thinking approach to ensure that your business stays secure, efficient, and ready for the future.
        </p>
        <p class="footer-text">Successfully Providing the Best Business Solution from 3 years</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-us-section {
  padding: 80px 0;
  background-color: white;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 15px;
}

.about-content {
  display: flex;
  gap: 60px;
  align-items: center;
}

/* Image Grid */
.image-grid {
  flex: 1;
  display: flex;
  gap: 20px;
}

.image-col-1, .image-col-2 {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.image-col-1 {
  margin-top: 0;
}

.image-col-2 {
  margin-top: 40px; /* Offset for staggered look */
}

.about-img {
  width: 100%;
  border-radius: 0; /* Reset default radius if any */
  object-fit: cover;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.img-1 {
  height: 200px;
  border-top-left-radius: 40px;
}

.img-2 {
  height: 150px;
}

.img-3 {
  height: 150px;
}

.img-4 {
  height: 200px;
  border-bottom-right-radius: 40px;
}

/* Text Content */
.text-content {
  flex: 1;
}

.section-header {
  background-color: #004799;
  display: block;
  width: 100%;
  padding: 10px 0;
  margin-bottom: 20px;
  text-align: center;
}

.section-header h2 {
  color: white;
  margin: 0;
  font-size: 18px;
  font-weight: 700;
  text-transform: uppercase;
}

.text-content h3 {
  color: #004799;
  font-size: 32px;
  font-weight: 600;
  margin-bottom: 20px;
  line-height: 1.3;
}

.description {
  color: #666;
  font-size: 16px;
  line-height: 1.8;
  margin-bottom: 20px;
  text-align: justify;
}

.footer-text {
  color: #34BB78; /* Green */
  font-weight: 600;
  font-size: 14px;
}

/* Responsive */
@media (max-width: 992px) {
  .about-content {
    flex-direction: column;
  }
  
  .image-grid {
    width: 100%;
    justify-content: center;
  }
  
  .text-content {
    width: 100%;
  }
}

@media (max-width: 576px) {
  .image-grid {
    gap: 10px;
  }
  
  .image-col-1, .image-col-2 {
    gap: 10px;
  }
  
  .text-content h3 {
    font-size: 24px;
  }
}
</style>
