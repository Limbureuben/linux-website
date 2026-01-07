<template>
  <section class="contact-us-section">
    <div class="container">
      <div class="contact-grid">
        <!-- Contact Form -->
        <div class="contact-form-container animate-fade-up">
          <h2 class="form-title">Send Us a Message</h2>
          <form @submit.prevent="handleSubmit" class="contact-form">
            <div class="form-row">
              <div class="form-group">
                <input type="text" id="name" placeholder="Your Name" required />
              </div>
              <div class="form-group">
                <input type="email" id="email" placeholder="Email Address" required />
              </div>
            </div>
            <div class="form-group">
              <input type="tel" id="phone" placeholder="Phone Number" />
            </div>
            <div class="form-group">
              <textarea id="message" rows="5" placeholder="Message" required></textarea>
            </div>
            <button type="submit" class="submit-btn hover-glow">Send Message</button>
          </form>
        </div>

        <!-- Contact Info Card -->
        <div class="contact-info-card animate-fade-up" style="transition-delay: 0.2s">
          <div class="info-header">
            <h3>CONTACT INFORMATION</h3>
          </div>
          <div class="info-body">
            <div class="info-item">
              <div class="info-icon">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path><circle cx="12" cy="10" r="3"></circle></svg>
              </div>
              <div class="info-text">
                <h4>Address</h4>
                <p>Posta, Kinondoni<br>Dar es salaam, Tanzania</p>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path></svg>
              </div>
              <div class="info-text">
                <h4>Phone</h4>
                <p>+255 621889899<br>+255 625219727</p>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 1 1-7.6-11.7 8.38 8.38 0 0 1 3.8.9L21 3z"></path></svg>
              </div>
              <div class="info-text">
                <h4>WhatsApp</h4>
                <p>+255 621889899</p>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
              </div>
              <div class="info-text">
                <h4>Email</h4>
                <p>limbureubenn@gmail.com</p>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>
              </div>
              <div class="info-text">
                <h4>Office hour</h4>
                <p>Mon - Sun, 8:00AM - 6:00PM</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const handleSubmit = () => {
  alert('Thank you for your message! We will get back to you soon.')
}
</script>

<style scoped>
.contact-us-section {
  padding: 80px 0;
  background-color: #F8FAFC;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 30px;
  align-items: start;
}

/* Form Styling */
.contact-form-container {
  background: white;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
}

.form-title {
  font-size: clamp(20px, 3vw, 24px);
  font-weight: 700;
  color: #004799;
  margin-bottom: 25px;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 12px 15px;
  border: 1px solid #E2E8F0;
  border-radius: 6px;
  background-color: #F8FAFC;
  font-family: 'Outfit', sans-serif;
  font-size: 15px;
  color: #4A5568;
  transition: all 0.3s ease;
  box-sizing: border-box;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #004799;
  background-color: white;
  box-shadow: 0 0 0 3px rgba(0, 71, 153, 0.1);
}

.submit-btn {
  background-color: #004799;
  color: white;
  padding: 12px 30px;
  border: none;
  border-radius: 6px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  align-self: flex-start;
}

.submit-btn:hover {
  background-color: #002a5c;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 71, 153, 0.2);
}

/* Info Card Styling */
.contact-info-card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
}

.info-header {
  background-color: #004799;
  padding: 20px;
  text-align: center;
}

.info-header h3 {
  color: white;
  font-size: 16px;
  font-weight: 700;
  margin: 0;
  letter-spacing: 1px;
}

.info-body {
  padding: 30px;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.info-item {
  display: flex;
  gap: 15px;
  align-items: flex-start;
}

.info-icon {
  color: #004799;
  background: #f0f7ff;
  width: 45px;
  height: 45px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.info-icon svg {
  width: 22px;
  height: 22px;
}

.info-text h4 {
  font-size: 15px;
  font-weight: 700;
  color: #1A202C;
  margin: 0 0 5px 0;
}

.info-text p {
  font-size: 14px;
  color: #4A5568;
  line-height: 1.6;
  margin: 0;
}

/* Responsive */
@media (max-width: 992px) {
  .contact-grid {
    grid-template-columns: 1fr;
    max-width: 700px;
    margin: 0 auto;
  }
}

@media (max-width: 600px) {
  .contact-us-section {
    padding: 60px 0;
  }

  .form-row {
    grid-template-columns: 1fr;
    gap: 15px;
  }
  
  .contact-form-container {
    padding: 25px;
  }
  
  .info-body {
    padding: 25px;
  }

  .submit-btn {
    width: 100%;
  }
}
</style>
