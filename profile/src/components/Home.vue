<template>
  <div class="profile-container" style="padding-left: 200px;">
    <div class="profile-sidebar">
      <div class="profile-image-container">
        <img src="./img/mahad.jpg" alt="Mahad Idrees Khan" class="profile-image" />
        <div class="image-overlay"></div>
      </div>
    </div>
    
    <div class="content-main" style="padding-left: 200px;padding-top: 120px;">
      <div class="header-section" >
        <h1>Mahad Idrees Khan</h1>
        <p class="subtitle">Technology Enthusiast • Software Engineer • Frontend Developer</p>
        <div class="social-links">
          <a href="https://github.com/MahadIdrees2004/" target="_blank" class="social-btn">GitHub</a>
          <a href="https://www.linkedin.com/in/mahad-idrees-khan-643687250/" target="_blank" class="social-btn">LinkedIn</a>
          <a href="mailto:mahadidrees2004@gmail.com" class="social-btn">Email</a>
        </div>
      </div>

      <div class="about-section">
        <h2>About Me</h2>
        <div class="about-content">
          <p class="intro">👋 Hi there! I'm <span class="highlight">Mahad Idrees Khan</span></p>
          <p class="main-desc">A creative full-stack developer and aspiring Computer Science student at UET (2023-2027). I blend innovative design with cutting-edge technology to craft exceptional digital experiences.</p>
          <p class="passion">My passion lies in transforming ideas into reality through clean code and intuitive interfaces. Whether it's building responsive web apps or exploring AI solutions, I'm always excited to embrace new challenges and push the boundaries of what's possible.</p>
        </div>
      </div>

      <div class="info-section" style="max-width: 400px;">
        <div class="info-grid">
          <div class="info-item">
            <span class="info-label">👨‍👦 Father</span>
            <span class="info-value">Muhammad Idrees Khan</span>
          </div>
          <div class="info-item">
            <span class="info-label">🎂 Age</span>
            <span class="info-value">18</span>
          </div>
          <div class="info-item">
            <span class="info-label">📞 Phone</span>
            <span class="info-value">0313-4384605</span>
          </div>
          <div class="info-item">
            <span class="info-label">🏠 Address</span>
            <span class="info-value">479-K, Al-Rehman Garden Phase II, Lahore</span>
          </div>
          <div class="info-item">
            <span class="info-label">✉️ Email</span>
            <span class="info-value">mahadidrees2004email.com</span>
          </div>
          <div class="info-item">
            <span class="info-label">💡 Interests</span>
            <span class="info-value">Coding, Communication, Football, Reading</span>
          </div>
        </div>
      </div>

      <div class="action-buttons">
        <a href="#/Projects" class="action-btn">View Projects</a>
        <a href="#/Skills" class="action-btn">My Skills</a>
      </div>
    </div>
  </div>
  <br>
  <br>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

.profile-container {
  display: flex;
  min-height: 100vh;
  background: linear-gradient(135deg, rgb(0, 0, 0) 0%, #000000 100%);
  color: #e0e4eb;
  font-family: 'Inter', sans-serif;
  animation: fadeIn 0.8s ease-out;
  position: relative;
  overflow: hidden;
}

.profile-container::before {
  content: '';
  position: absolute;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle at center, rgb(0,0,0) 0%, transparent 50%);
  animation: rotateBackground 20s linear infinite;
  z-index: 0;
}

@keyframes rotateBackground {
  0% { transform: translate(-50%, -50%) rotate(0deg); }
  100% { transform: translate(-50%, -50%) rotate(360deg); }
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.profile-sidebar {
  width: 400px;
  background: rgba(0, 0, 0, 0.2);
  position: fixed;
  height: 100vh;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  border-right: 1px solid rgba(0, 0, 0, 0.2);
  box-shadow: 2px 0 30px rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(20px);
  animation: slideInLeft 1s ease-out;
  z-index: 2;
  overflow: hidden;
}

@keyframes slideInLeft {
  from { transform: translateX(-100%); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

.profile-image {
  width: 100%;
  height: 100vh;
  object-fit: cover;
  border: none;
  animation: profileImageLoad 1.2s ease-out;
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  filter: brightness(1) contrast(1);
}

.profile-image-container {
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
}

.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(
    45deg,
    rgba(0, 0, 0, 0.1),
    rgba(0, 0, 0, 0.05)
  );
  z-index: 1;
}

.profile-image:hover {
  transform: scale(1.1);
}

@keyframes profileImageLoad {
  from { transform: scale(1.2); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

.social-links {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.social-btn {
  padding: 12px 20px;
  background: rgba(30, 41, 59, 0.8);
  color: #94a3b8;
  text-decoration: none;
  border-radius: 8px;
  text-align: center;
  font-weight: 500;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid rgba(59, 130, 246, 0.2);
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(8px);
  letter-spacing: 0.5px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.social-btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.8) 50%, rgba(255,255,255,0) 100%);
  transition: all 0.6s ease;
}

.social-btn:hover {
  background: rgba(59, 130, 246, 0.15);
  transform: translateY(-2px);
  box-shadow: 0 4px 20px rgba(59, 130, 246, 0.3);
  color: #ffffff;
  border-color: rgba(59, 130, 246, 0.5);
}

.social-btn::after {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle at center, rgba(59, 130, 246, 0.2), transparent 50%);
  opacity: 0;
  transition: opacity 0.6s ease;
  transform: rotate(45deg);
}

.social-btn:hover::after {
  opacity: 1;
  animation: pulseGlow 2s infinite;
}

@keyframes pulseGlow {
  0% { transform: rotate(45deg) scale(1); opacity: 0.5; }
  50% { transform: rotate(45deg) scale(1.2); opacity: 0.2; }
  100% { transform: rotate(45deg) scale(1); opacity: 0.5; }
}

.content-main {
  margin-left: 400px;
  padding: 40px 60px;
  flex: 1;
  position: relative;
  z-index: 2;
  max-width: 1200px;
}

.header-section {
  margin-bottom: 30px;
  position: relative;
  padding-top: 20px;
}

.header-section h1 {
  font-size: 3rem;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 12px;
  text-shadow: 0 2px 10px rgba(59, 130, 246, 0.3);
  letter-spacing: -0.5px;
}

.subtitle {
  font-size: 1.2rem;
  color: #94a3b8;
  margin-bottom: 24px;
  letter-spacing: 0.5px;
}

.social-links {
  display: flex;
  gap: 12px;
  margin-top: 24px;
  max-width: 400px;
}

.about-section {
  margin-bottom: 30px;
  padding: 0 0 20px;
}

h2 {
  font-size: 1.8rem;
  font-weight: 600;
  color: #ffffff;
  margin-bottom: 20px;
  text-shadow: 0 2px 10px rgba(59, 130, 246, 0.3);
  position: relative;
  display: inline-block;
}

h2::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -6px;
  width: 40px;
  height: 3px;
  background: linear-gradient(90deg, #3b82f6, transparent);
  border-radius: 2px;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 25px;
  margin-bottom: 40px;
}

.project-card {
  background: linear-gradient(135deg, rgba(30, 41, 59, 0.8) 0%, rgba(15, 23, 42, 0.8) 100%);
  padding: 24px;
  border-radius: 16px;
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  border: 1px solid rgba(59, 130, 246, 0.2);
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(8px);
  transform-style: preserve-3d;
  perspective: 1000px;
}

.project-card::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(255,255,255,0.2) 0%, rgba(255,255,255,0) 100%);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.project-card:hover {
  transform: translateY(-4px) scale(1.02) rotateX(5deg);
  box-shadow: 0 8px 30px rgba(59, 130, 246, 0.3);
  border-color: rgba(59, 130, 246, 0.5);
}

.project-card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 50% 0%, rgba(59, 130, 246, 0.4), transparent 70%);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.project-card:hover::before {
  opacity: 0.5;
  animation: shimmer 2s infinite;
}

@keyframes shimmer {
  0% { transform: translateY(-100%); }
  100% { transform: translateY(100%); }
}

.project-card h3 {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 8px;
}

.tech-tag {
  display: inline-block;
  padding: 6px 14px;
  background: linear-gradient(135deg, rgba(59, 130, 246, 0.2) 0%, rgba(37, 99, 235, 0.2) 100%);
  border-radius: 20px;
  font-size: 0.9rem;
  color: #60a5fa;
  font-weight: 500;
  box-shadow: 0 2px 8px rgba(37, 99, 235, 0.2),
              0 0 0 1px rgba(59, 130, 246, 0.1);
  transition: all 0.3s ease;
  backdrop-filter: blur(4px);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.tech-tag:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.15);
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 15px;
  margin-bottom: 30px;
  padding: 0 0 20px;
}

.info-item {
  background: linear-gradient(135deg, rgba(30, 41, 59, 0.8) 0%, rgba(15, 23, 42, 0.8) 100%);
  padding: 20px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  gap: 8px;
  border: 1px solid rgba(59, 130, 246, 0.2);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(8px);
  transition: all 0.3s ease;
}

.info-item:hover {
  transform: translateY(-2px);
  border-color: rgba(59, 130, 246, 0.4);
  box-shadow: 0 8px 30px rgba(59, 130, 246, 0.15);
}

.info-label {
  font-size: 0.9rem;
  color: #94a3b8;
  font-weight: 500;
  letter-spacing: 0.5px;
}

.info-value {
  font-size: 1rem;
  color: #e2e8f0;
  font-weight: 400;
}

.action-buttons {
  display: flex;
  gap: 16px;
}

.action-btn {
  padding: 16px 32px;
  background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
  color: #ffffff;
  text-decoration: none;
  border-radius: 12px;
  font-weight: 600;
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  position: relative;
  overflow: hidden;
  box-shadow: 0 4px 20px rgba(59, 130, 246, 0.4),
              0 0 0 2px rgba(59, 130, 246, 0.2);
  text-transform: uppercase;
  letter-spacing: 1px;
  font-size: 0.9rem;
  border: none;
  backdrop-filter: blur(4px);
}

.action-btn::after {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(135deg, rgba(255,255,255,0.2) 0%, rgba(255,255,255,0) 60%);
  transform: rotate(45deg);
  opacity: 0;
  transition: opacity 0.6s ease;
}

.action-btn:hover {
  background: linear-gradient(135deg, #1d4ed8 0%, #1e40af 100%);
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(37, 99, 235, 0.25);
}

.action-btn:hover::after {
  opacity: 1;
}

@media (max-width: 768px) {
  .profile-container {
    flex-direction: column;
  }

  .profile-sidebar {
    position: relative;
    width: 100%;
    height: auto;
    padding: 15px;
    margin-bottom: 20px;
  }

  .content-main {
    margin-left: 0;
    padding: 20px 25px;
    width: 100%;
  }

  .profile-image {
    width: 150px;
    height: 150px;
  }

  .social-links {
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
  }

  .social-btn {
    min-width: 120px;
  }
}
</style>
