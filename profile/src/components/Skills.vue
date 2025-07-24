<template>
    <div class="skills-container">
        <h1 class="skills-title">My Skills & Expertise</h1>
        
        <div class="skills-grid">
            <!-- Programming Languages -->
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/py.jpg" alt="Python" class="skill-image" />
                </div>
                <div class="skill-name">Python</div>
            </div>
            
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/cpp.jpg" alt="C++" class="skill-image" />
                </div>
                <div class="skill-name">C++</div>
            </div>

            <!-- Web Technologies -->
             <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/vu.jpg" alt="Vue.js" class="skill-image" />
                </div>
                <div class="skill-name">Vue.js</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/html.jpg" alt="HTML" class="skill-image" />
                </div>
                <div class="skill-name">HTML</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/css.jpg" alt="CSS" class="skill-image" />
                </div>
                <div class="skill-name">CSS</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/node.jpg" alt="Python" class="skill-image" />
                </div>
                <div class="skill-name">Node.js</div>
            </div>

            <!-- Frameworks and Tools -->
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/bootstrap.logo.jpeg" alt="Bootstrap" class="skill-image" />
                </div>
                <div class="skill-name">Bootstrap</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/flask.jpg" alt="Flask" class="skill-image" />
                </div>
                <div class="skill-name">Flask</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/streamlit.jpg" alt="Streamlit" class="skill-image" />
                </div>
                <div class="skill-name">Streamlit</div>
            </div>

            <!-- Databases -->
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/mongodb.jpg" alt="MongoDB" class="skill-image" />
                </div>
                <div class="skill-name">MongoDB</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/sql.jpg" alt="SQL" class="skill-image" />
                </div>
                <div class="skill-name">SQL</div>
            </div>

            <!-- Development Tools -->
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/github.jpg" alt="GitHub" class="skill-image" />
                </div>
                <div class="skill-name">GitHub</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/npm.jpg" alt="NPM" class="skill-image" />
                </div>
                <div class="skill-name">NPM</div>
            </div>

            <!-- AI and Modeling -->
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/LLM.jpg" alt="Large Language Models" class="skill-image" />
                </div>
                <div class="skill-name">LLM</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/langchain.jpg" alt="LangChain" class="skill-image" />
                </div>
                <div class="skill-name">LangChain</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/uml.jpg" alt="UML Diagrams" class="skill-image" />
                </div>
                <div class="skill-name">UML</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./office.logo.png" alt="UML Diagrams" class="skill-image" />
                </div>
                <div class="skill-name">MS-Office</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/star.jpg" alt="UML Diagrams" class="skill-image" />
                </div>
                <div class="skill-name">Star UML</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/mend.jpg" alt="UML Diagrams" class="skill-image" />
                </div>
                <div class="skill-name">Mendeley Reference</div>
            </div>
            <div class="skill-card">
                <div class="skill-image-container">
                    <img src="./img/ass.jpg" alt="UML Diagrams" class="skill-image" />
                </div>
                <div class="skill-name">Assembly Language</div>
            </div>
        </div>

       
    </div>
</template>

<style scoped>
.skills-container {
    padding: 40px;
    background: linear-gradient(135deg, rgb(0, 0, 0) 0%, #000000 100%);
    color: #e0e4eb;
    min-height: 100vh;
    animation: fadeIn 0.8s ease-out;
}

.skills-title {
    font-size: 2.5rem;
    font-weight: 700;
    color: #ffffff;
    margin-bottom: 40px;
    text-align: center;
    text-shadow: 0 2px 10px rgba(59, 130, 246, 0.3);
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
}

.skill-card {
    background: rgba(30, 41, 59, 0.8);
    border-radius: 16px;
    overflow: hidden;
    backdrop-filter: blur(8px);
    border: 1px solid rgba(59, 130, 246, 0.2);
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    display: flex;
    flex-direction: column;
}

.skill-card:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 8px 30px rgba(59, 130, 246, 0.3);
    border-color: rgba(59, 130, 246, 0.5);
}

.skill-image-container {
    aspect-ratio: 16/9;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    background: rgba(15, 23, 42, 0.5);
}

.skill-image {
    width: 100%;
    height: 100%;
    object-fit: contain;
    transition: transform 0.4s ease;
}

.skill-card:hover .skill-image {
    transform: scale(1.1);
}

.skill-name {
    padding: 12px;
    text-align: center;
    color: #e0e4eb;
    font-weight: 500;
    font-size: 1.1rem;
    background: rgba(15, 23, 42, 0.9);
    border-top: 1px solid rgba(59, 130, 246, 0.2);
    letter-spacing: 0.5px;
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

.skill-category h2 {
    font-size: 1.5rem;
    color: #ffffff;
    margin-bottom: 20px;
    position: relative;
    display: inline-block;
}

.skill-category h2::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -6px;
    width: 40px;
    height: 3px;
    background: linear-gradient(90deg, #3b82f6, transparent);
    border-radius: 2px;
}

.skills-items {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.skill-item {
    background: rgba(15, 23, 42, 0.6);
    padding: 15px;
    border-radius: 12px;
    border: 1px solid rgba(59, 130, 246, 0.1);
}

.skill-header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
}

.skill-name {
    color: #e2e8f0;
    font-weight: 500;
}

.skill-level {
    color: #60a5fa;
    font-size: 0.9rem;
}

.progress-bar {
    height: 6px;
    background: rgba(59, 130, 246, 0.2);
    border-radius: 3px;
    overflow: hidden;
}

.progress {
    height: 100%;
    background: linear-gradient(90deg, #3b82f6, #1d4ed8);
    border-radius: 3px;
    transition: width 1s ease-in-out;
}

.certificates-section {
    margin-top: 60px;
}

.certificates-section h2 {
    font-size: 2rem;
    color: #ffffff;
    margin-bottom: 30px;
    text-align: center;
}

.certificates-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
}

.certificate-card {
    background: rgba(30, 41, 59, 0.8);
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid rgba(59, 130, 246, 0.2);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.certificate-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 30px rgba(59, 130, 246, 0.2);
}

.certificate-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.certificate-content {
    padding: 20px;
}

.certificate-content h3 {
    color: #ffffff;
    margin-bottom: 8px;
}

.certificate-content p {
    color: #94a3b8;
    font-size: 0.9rem;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

@media (max-width: 768px) {
    .skills-container {
        padding: 20px;
    }

    .skills-grid {
        grid-template-columns: 1fr;
        gap: 20px;
    }

    .certificates-grid {
        grid-template-columns: 1fr;
    }
}
</style>