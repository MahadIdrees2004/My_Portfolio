<template>
<div class="projects-container">
    <h1 class="projects-title">Project Journey</h1>

    <div class="timeline-container">
        <!-- Portfolio Website -->
        <div class="project-item left">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'portfolio' }" @click="toggleDescription('portfolio')">
                <div class="card-header">
                    <img src="./img/vu.jpg" alt="Vue.js" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">July - Sept 2025</span>
                        <h2>Personal Portfolio Website</h2>
                    </div>
                </div>
                <div class="card-body">
                    <div class="description">
                        <p>Modern, responsive portfolio showcasing my projects and skills, built with Vue.js and featuring glass-morphism design.</p>
                        <div class="project-links">
                            
                            <a href="https://github.com/MahadIdrees2004/My_Portfolio" target="_blank" class="project-link">GitHub Repo</a>
                        </div>
                        <div class="tech-stack">
                            <span class="tech-tag">Vue.js</span>
                            <span class="tech-tag">CSS3</span>
                            <span class="tech-tag">Responsive Design</span>
                            <span class="tech-tag">Glass UI</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Vue.js Todo App -->
        <div class="project-item right">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'todo' }" @click="toggleDescription('todo')">
                <div class="card-header">
                    <img src="./img/vue.jpg" alt="Vue.js" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">June - July 2025</span>
                        <h2>Vue.js 3 To-Do List App</h2>
                    </div>
                </div>
                <div class="card-body">
                    <div class="description">
                        <p>Modern task management app built with Vue 3 Composition API, featuring real-time updates and seamless task handling.</p>
                        <div class="project-links">
                            <a href="https://todo-app-kappa-bice-10.vercel.app/" target="_blank" class="project-link">Live Demo</a>
                            <a href="https://github.com/MahadIdrees2004/todo-app" target="_blank" class="project-link">GitHub Repo</a>
                        </div>
                        <div class="tech-stack">
                            <span class="tech-tag">Vue.js</span>
                            <span class="tech-tag">Composition API</span>
                            <span class="tech-tag">Vercel</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Restaurant Name Generator -->
        <div class="project-item left">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'restaurant' }" @click="toggleDescription('restaurant')">
                <div class="card-header">
                    <img src="./img/LLM.jpg" alt="LLM" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">May - June 2025</span>
                        <h2>Restaurant Name Generator</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'restaurant' }">
                    <div class="description">
                        <p>🚀 A unique Restaurant Name & Menu Generator web app using custom-configured LLM and Streamlit.</p>
                        <h3>🔍 Features:</h3>
                        <ul>
                            <li>Dynamic cuisine-based name generation</li>
                            <li>Authentic menu suggestions</li>
                            <li>Custom LLM integration</li>
                        </ul>
                        <div class="project-links">
                            <a href="https://restaurant-name-and-menu-generator.streamlit.app/" target="_blank" class="project-link">Live Demo</a>
                            <a href="https://github.com/MahadIdrees2004/Restaurant_Name_and_Menu_Generator" target="_blank" class="project-link">GitHub Repo</a>
                        </div>
                        <div class="tech-stack">
                            <span class="tech-tag">LangChain</span>
                            <span class="tech-tag">Streamlit</span>
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Gemini</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Query Load Balancer -->
        <div class="project-item right">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'loadbalancer' }" @click="toggleDescription('loadbalancer')">
                <div class="card-header">
                    <img src="./img/py.jpg" alt="Flask" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Jan - Apr 2025</span>
                        <h2>Query Load Balancer</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'loadbalancer' }">
                    <div class="description">
                        <p>Intelligent system that distributes database queries across multiple servers for optimal performance and load balancing.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">Flask</span>
                            <span class="tech-tag">SQLite</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">Bootstrap</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Event Management System -->
        <div class="project-item left">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'event' }" @click="toggleDescription('event')">
                <div class="card-header">
                    <img src="./img/cpp.jpg" alt="UET" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Sep - Dec 2024</span>
                        <h2>Event Management System</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'event' }">
                    <div class="description">
                        <p>Streamlined event booking system with role-based access for administrators, workers, and customers to manage bookings efficiently.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">C++</span>
                            <span class="tech-tag">OOP</span>
                            <span class="tech-tag">UML</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Bank Management System -->
        <div class="project-item right">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'bank' }" @click="toggleDescription('bank')">
                <div class="card-header">
                    <img src="./img/dsa.jpg" alt="UET" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Sep - Dec 2024</span>
                        <h2>Bank Management System</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'bank' }">
                    <div class="description">
                        <p>Banking system implementing advanced data structures for efficient transaction management and secure account operations.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">Data Structures</span>
                            <span class="tech-tag">Algorithms</span>
                            <span class="tech-tag">DSA</span>
                            <span class="tech-tag">C++</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Office Management Network -->
        <div class="project-item left">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'network' }" @click="toggleDescription('network')">
                <div class="card-header">
                    <img src="./img/cn.jpg" alt="UET" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Nov - Dec 2024</span>
                        <h2>Office Management Network</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'network' }">
                    <div class="description">
                        <p>Enterprise network architecture featuring floor-wise network segmentation and dedicated access points for 8 departments.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">Computer Networking</span>
                            <span class="tech-tag">Network Design</span>
                            <span class="tech-tag">Network Switches</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Combinational Lock System -->
        <div class="project-item right">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'lock' }" @click="toggleDescription('lock')">
                <div class="card-header">
                    <img src="./img/dld.jpg" alt="UET" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Mar - May 2024</span>
                        <h2>Combinational Lock System</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'lock' }">
                    <div class="description">
                        <p>Digital security system implementing 8-bit combination logic for secure access control and state validation.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">Logic Design</span>
                            <span class="tech-tag">Digital Logic</span>
                            <span class="tech-tag">Team Leadership</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Library Management System -->
        <div class="project-item left">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'library' }" @click="toggleDescription('library')">
                <div class="card-header">
                    <img src="./img/sq.jpg" alt="Database" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Jan - Apr 2024</span>
                        <h2>Library Management System</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'library' }">
                    <div class="description">
                        <p>Database system with optimized schema design for managing books, members, and lending operations in a library.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">DBMS</span>
                            <span class="tech-tag">SQL</span>
                            <span class="tech-tag">Schema Design</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Car Rental Management System -->
        <div class="project-item right">
            <div class="timeline-dot"></div>
            <div class="project-card" :class="{ 'active': activeProject === 'car' }" @click="toggleDescription('car')">
                <div class="card-header">
                    <img src="./img/cpp.jpg" alt="UET" class="project-logo">
                    <div class="header-content">
                        <span class="year-badge">Nov - Dec 2023</span>
                        <h2>Car Rental Management System</h2>
                    </div>
                </div>
                <div class="card-body" :class="{ 'show-description': activeProject === 'car' }">
                    <div class="description">
                        <p>Console application for managing vehicle rentals, inventory, and customer bookings with an intuitive interface.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">C++</span>
                            <span class="tech-tag">Programming</span>
                            <span class="tech-tag">Team Leadership</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script setup>
import { ref } from 'vue'

const activeProject = ref(null)

const toggleDescription = (projectId) => {
    activeProject.value = activeProject.value === projectId ? null : projectId
}
</script>

<style scoped>
.projects-container {
    padding: 40px;
    background: linear-gradient(135deg, rgb(0, 0, 0) 0%, #000000 100%);
    color: #e0e4eb;
    min-height: 100vh;
    animation: fadeIn 0.8s ease-out;
}

.projects-title {
    font-size: 2.5rem;
    font-weight: 700;
    color: #ffffff;
    margin-bottom: 40px;
    text-align: center;
    text-shadow: 0 2px 10px rgba(59, 130, 246, 0.3);
}

.timeline-container {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

.timeline-container::after {
    content: '';
    position: absolute;
    width: 2px;
    background: linear-gradient(to bottom, transparent, #3b82f6, transparent);
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -1px;
    animation: glowLine 2s ease-in-out infinite;
}

@keyframes glowLine {
    0%, 100% { box-shadow: 0 0 5px #3b82f6; }
    50% { box-shadow: 0 0 20px #3b82f6; }
}

.project-item {
    padding: 10px 40px;
    position: relative;
    width: 50%;
    animation: fadeInSlide 0.6s ease-out forwards;
    opacity: 0;
}

.project-item.right {
    left: 50%;
}

.project-item.left {
    left: 0;
}

.timeline-dot {
    width: 20px;
    height: 20px;
    background: #3b82f6;
    border-radius: 50%;
    position: absolute;
    right: -50px;
    top: 50%;
    transform: translateY(-50%);
    z-index: 2;
    box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.2);
}

.project-item.right .timeline-dot {
    left: -50px;
}

.project-card {
    background: rgba(30, 41, 59, 0.8);
    border-radius: 16px;
    overflow: hidden;
    backdrop-filter: blur(8px);
    border: 1px solid rgba(59, 130, 246, 0.2);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    cursor: pointer;
}

.project-card:hover {
    transform: translateY(-5px);
    border-color: rgba(59, 130, 246, 0.5);
    box-shadow: 0 8px 30px rgba(59, 130, 246, 0.2);
}

.card-header {
    padding: 20px;
    display: flex;
    align-items: center;
    gap: 15px;
    background: rgba(15, 23, 42, 0.6);
}

.project-logo {
    width: 60px;
    height: 60px;
    border-radius: 12px;
    object-fit: cover;
}

.header-content h2 {
    font-size: 1.2rem;
    margin-top: 8px;
    color: #ffffff;
    letter-spacing: 0.5px;
}

.year-badge {
    background: rgba(59, 130, 246, 0.2);
    padding: 4px 12px;
    border-radius: 12px;
    font-size: 0.9rem;
    color: #60a5fa;
    display: inline-block;
    margin-bottom: 10px;
    border: 1px solid rgba(59, 130, 246, 0.1);
}

.card-body {
    opacity: 0;
    height: 0;
    overflow: hidden;
    transition: all 0.3s ease-out;
}

.project-card:hover .card-body,
.project-card.active .card-body {
    opacity: 1;
    height: auto;
    min-height: 120px;
}

.project-card.active {
    border-color: rgba(59, 130, 246, 0.5);
    box-shadow: 0 8px 30px rgba(59, 130, 246, 0.2);
}

.description {
    padding: 20px;
}

.description p {
    margin-bottom: 15px;
    line-height: 1.6;
}

.description ul {
    margin: 15px 0;
    padding-left: 20px;
}

.description li {
    margin-bottom: 8px;
    color: #94a3b8;
}

.project-links {
    display: flex;
    gap: 10px;
    margin: 15px 0;
}

.project-link {
    padding: 8px 16px;
    background: rgba(59, 130, 246, 0.2);
    color: #60a5fa;
    text-decoration: none;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.project-link:hover {
    background: rgba(59, 130, 246, 0.3);
    transform: translateY(-2px);
}

.project-link.disabled {
    opacity: 0.6;
    cursor: not-allowed;
    pointer-events: none;
    position: relative;
}

.project-link.disabled:hover::after {
    content: attr(title);
    position: absolute;
    bottom: 100%;
    left: 50%;
    transform: translateX(-50%);
    padding: 4px 8px;
    background: rgba(15, 23, 42, 0.9);
    border-radius: 4px;
    font-size: 0.8rem;
    white-space: nowrap;
}

.tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 15px;
}

.tech-tag {
    padding: 4px 12px;
    background: rgba(59, 130, 246, 0.1);
    color: #60a5fa;
    border-radius: 20px;
    font-size: 0.9rem;
    border: 1px solid rgba(59, 130, 246, 0.2);
}

@keyframes fadeInSlide {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@media (max-width: 768px) {
    .timeline-container::after {
        left: 31px;
    }

    .project-item {
        width: 100%;
        padding-left: 70px;
        padding-right: 20px;
    }

    .project-item.right {
        left: 0;
    }

    .timeline-dot {
        left: 22px;
    }

    .project-item.right .timeline-dot {
        left: 22px;
    }

    .projects-container {
        padding: 20px;
    }

    .card-header {
        flex-direction: column;
        text-align: center;
    }

    .project-logo {
        width: 80px;
        height: 80px;
    }
}
</style>