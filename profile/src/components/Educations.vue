<template>
<div class="educations-container">
  <h1 class="educations-title">Educational Journey</h1>
  
  <div class="timeline-container">
    <div class="education-item right">
      <div class="timeline-dot"></div>
      <div class="education-card">
        <div class="card-header">
          <img src="./img/uet.jpg" alt="UET Logo" class="institution-logo">
          <div class="header-content">
            <span class="year-badge">2023 - Present</span>
            <h2>Bachelors in Computer Science</h2>
          </div>
        </div>
        <div class="card-body">
          <h3>University of Engineering & Technology</h3>
          <div class="highlight-bar"></div>
          <p class="institution-location">Lahore, Pakistan</p>
        </div>
      </div>
    </div>

    <div class="education-item left">
      <div class="timeline-dot"></div>
      <div class="education-card">
        <div class="card-header">
          <img src="./img/clg.jpg" alt="College Logo" class="institution-logo">
          <div class="header-content">
            <span class="year-badge">2020 - 2022</span>
            <h2>Intermediate in Computer Science</h2>
          </div>
        </div>
        <div class="card-body">
          <h3>Government College of Science</h3>
          <div class="highlight-bar"></div>
          <p class="institution-location">Wahdat Road, Lahore</p>
        </div>
      </div>
    </div>

    <div class="education-item right">
      <div class="timeline-dot"></div>
      <div class="education-card">
        <div class="card-header">
          <img src="./img/sch.jpg" alt="School Logo" class="institution-logo">
          <div class="header-content">
            <span class="year-badge">2018 - 2020</span>
            <h2>Matriculation in Computer Science</h2>
          </div>
        </div>
        <div class="card-body">
          <h3>Government Pilot Higher Secondary School</h3>
          <div class="highlight-bar"></div>
          <p class="institution-location">Wahdat Colony, Lahore</p>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
.educations-container {
  padding: 40px 0;
  width: 100%;
  position: relative;
  overflow: hidden;
}

.educations-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: radial-gradient(circle at top right, rgba(59, 130, 246, 0.1), transparent 60%);
  pointer-events: none;
}

.educations-title {
  font-size: 2.5rem;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 60px;
  text-align: center;
  text-shadow: 0 2px 10px rgba(59, 130, 246, 0.3);
  letter-spacing: -0.5px;
  position: relative;
  animation: titlePulse 2s infinite;
}

.timeline-container {
  position: relative;
  width: 100%;
  padding: 20px 100px;
  box-sizing: border-box;
}

.timeline-container::after {
  content: '';
  position: absolute;
  width: 6px;
  background: linear-gradient(180deg, #3b82f6, rgba(59, 130, 246, 0.1));
  top: 0;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 3px;
  animation: timelineGlow 2s infinite;
}

.timeline-dot {
  width: 20px;
  height: 20px;
  background: #3b82f6;
  border-radius: 50%;
  position: absolute;
  right: -10px;
  top: 30px;
  transform: translateY(-50%);
  z-index: 2;
  box-shadow: 0 0 20px rgba(59, 130, 246, 0.6);
  animation: dotPulse 2s infinite;
}

.education-item {
  padding: 10px 60px;
  position: relative;
  width: 50%;
  margin-bottom: 30px;
  opacity: 0;
  animation: slideIn 0.8s ease forwards;
  box-sizing: border-box;
}

.education-item.left {
  left: 0;
  padding-right: 40px;
}

.education-item.right {
  left: 50%;
  padding-left: 40px;
}

.education-item.left .timeline-dot {
  right: -10px;
}

.education-item.right .timeline-dot {
  left: -10px;
}

.education-item:nth-child(1) { animation-delay: 0.3s; }
.education-item:nth-child(2) { animation-delay: 0.6s; }
.education-item:nth-child(3) { animation-delay: 0.9s; }

.education-card {
  background: rgba(15, 23, 42, 0.8);
  border-radius: 16px;
  overflow: hidden;
  backdrop-filter: blur(12px);
  border: 1px solid rgba(59, 130, 246, 0.2);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.3);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.education-card:hover {
  transform: translateY(-5px) scale(1.02);
  border-color: rgba(59, 130, 246, 0.4);
  box-shadow: 0 8px 30px rgba(59, 130, 246, 0.2);
}

.card-header {
  background: rgba(30, 41, 59, 0.9);
  padding: 20px;
  display: flex;
  align-items: center;
  gap: 20px;
  border-bottom: 1px solid rgba(59, 130, 246, 0.2);
}

.education-content:hover {
  transform: translateY(-5px);
  border-color: rgba(59, 130, 246, 0.4);
  box-shadow: 0 8px 30px rgba(59, 130, 246, 0.15);
}

.logo-container {
  position: relative;
  width: 100px;
  height: 100px;
  flex-shrink: 0;
}

.education-logo {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 12px;
  position: relative;
  z-index: 1;
}

.logo-glow {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at center, rgba(59, 130, 246, 0.3), transparent 70%);
  filter: blur(10px);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.education-content:hover .logo-glow {
  opacity: 1;
}

.education-details {
  flex: 1;
}

.education-institution {
  font-size: 1.4rem;
  font-weight: 600;
  color: #ffffff;
  margin-bottom: 8px;
  text-shadow: 0 2px 8px rgba(59, 130, 246, 0.2);
}

.education-degree {
  font-size: 1.1rem;
  color: #94a3b8;
  margin-bottom: 8px;
  letter-spacing: 0.5px;
}

.education-duration {
  display: inline-block;
  padding: 6px 14px;
  background: rgba(59, 130, 246, 0.15);
  color: #60a5fa;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 0.5px;
}

@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.institution-logo {
  width: 60px;
  height: 60px;
  border-radius: 12px;
  object-fit: cover;
  border: 2px solid rgba(59, 130, 246, 0.3);
  transition: transform 0.3s ease;
}

.education-card:hover .institution-logo {
  transform: scale(1.1);
}

.header-content {
  flex: 1;
}

.header-content h2 {
  font-size: 1.2rem;
  font-weight: 600;
  color: #ffffff;
  margin: 0;
  margin-bottom: 5px;
}

.year-badge {
  display: inline-block;
  padding: 4px 12px;
  background: rgba(59, 130, 246, 0.15);
  color: #60a5fa;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
  margin-bottom: 8px;
}

.card-body {
  padding: 20px;
  position: relative;
}

.card-body h3 {
  font-size: 1.1rem;
  color: #94a3b8;
  margin: 0;
  margin-bottom: 15px;
}

.highlight-bar {
  width: 40px;
  height: 3px;
  background: linear-gradient(90deg, #3b82f6, transparent);
  margin-bottom: 15px;
  border-radius: 2px;
}

.institution-location {
  color: #64748b;
  font-size: 0.9rem;
  margin: 0;
}

@keyframes timelineGlow {
  0%, 100% { box-shadow: 0 0 15px rgba(59, 130, 246, 0.3); }
  50% { box-shadow: 0 0 25px rgba(59, 130, 246, 0.5); }
}

@keyframes dotPulse {
  0%, 100% { box-shadow: 0 0 0 0 rgba(59, 130, 246, 0.4); }
  50% { box-shadow: 0 0 0 8px rgba(59, 130, 246, 0); }
}

@keyframes titlePulse {
  0%, 100% { text-shadow: 0 0 15px rgba(59, 130, 246, 0.3); }
  50% { text-shadow: 0 0 25px rgba(59, 130, 246, 0.5); }
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 768px) {
  .timeline-container {
    padding: 20px 30px;
  }

  .timeline-container::after {
    left: 31px;
  }

  .education-item {
    width: 100%;
    padding-left: 70px;
    padding-right: 20px;
  }

  .education-item.left,
  .education-item.right {
    left: 0;
  }

  .timeline-dot {
    left: 22px;
    right: auto;
  }

  .educations-title {
    font-size: 2rem;
  }

  .card-header {
    padding: 15px;
  }

  .institution-logo {
    width: 50px;
    height: 50px;
  }

  .header-content h2 {
    font-size: 1.1rem;
  }
}
</style>