<!-- Hero Section -->
<template>
    <section class="hero">

        <!-- Background Glow -->
        <div class="glow glow-1"></div>
        <div class="glow glow-2"></div>

        <div class="container">

            <!-- Left Content -->
            <div class="content" data-aos="fade-up">

                <!-- Availability Badge -->
                <div class="badge">
                    ● Available for Work
                </div>

                <!-- Name -->
                <h1 class="title">
                    Hi, I'm <span>Sakiru Akande</span>
                </h1>

                <!-- Role Animation -->
                <h2 class="subtitle">
                    <span ref="typedEl"></span>
                </h2>

                <!-- Description -->
                <p class="desc">
                    I build scalable <strong>ERP systems</strong>,
                    <strong>SaaS platforms</strong>, Payment Gateway Integration, Digital solutions and
                    <strong>enterprise web applications</strong> using Laravel, Vue.js and modern web technologies.
                </p>

                <!-- CTA Buttons -->
                <div class="actions">
                    <a href="#projects" class="btn primary">View Projects</a>
                    <a href="#contact" class="btn secondary">Hire Me</a>
                    <a :href="cvFile" target="_blank" class="btn cv-btn">
                        📄 View Resume
                    </a>
                </div>

            </div>

            <!-- Right Card -->
            <div class="card" data-aos="zoom-in">

                <div class="card-inner">

                    <h3>Software Engineer</h3>

                    <ul>
                        <li>✔ Laravel Expert</li>
                        <li>✔ Vue.js Developer</li>
                        <li>✔ API Architect</li>
                        <li>✔ EdTech Specialist</li>
                    </ul>

                    <div class="stats">
                        <div>
                            <h4>3+</h4>
                            <p>Years</p>
                        </div>
                        <div>
                            <h4>10+</h4>
                            <p>Projects</p>
                        </div>
                        <div>
                            <h4>6+</h4>
                            <p>Systems</p>
                        </div>
                    </div>

                </div>

            </div>

        </div>
    </section>
</template>

<script setup>
import Typed from "typed.js";
import { ref, onMounted } from "vue";
import cvFile from "../assets/files/AKANDE_SAKIRU_CV_LATEST.pdf";


const typedEl = ref(null);

onMounted(() => {
    new Typed(typedEl.value, {
        strings: [
            "Laravel Developer & Expert",
            "Vue.js Engineer & Specialist",
            "API Architect",
            "SaaS Builder & Architect",
            "EdTech System Developer",
        ],
        typeSpeed: 50,
        backSpeed: 60,
        loop: true,
    });
});
</script>

<style scoped>
.hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    background: #020617;
    overflow: hidden;
    color: white;
}

/* Container */
.container {
    width: 100%;
    max-width: 1200px;
    margin: auto;
    padding: 0 24px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
}

/* Glow Effects */
.glow {
    position: absolute;
    width: 400px;
    height: 400px;
    filter: blur(120px);
    opacity: 0.4;
}

.glow-1 {
    background: #06b6d4;
    top: -100px;
    left: -100px;
}

.glow-2 {
    background: #2563eb;
    bottom: -120px;
    right: -120px;
}

/* Badge */
.badge {
    display: inline-block;
    padding: 8px 14px;
    border-radius: 999px;
    background: rgba(6, 182, 212, 0.15);
    color: #06b6d4;
    font-size: 13px;
    margin-bottom: 20px;
}

/* Title */
.title {
    font-size: 48px;
    font-weight: 800;
}

.title span {
    color: #06b6d4;
}

/* Subtitle */
.subtitle {
    font-size: 24px;
    margin-top: 10px;
    color: #cbd5e1;
    min-height: 40px;
}

/* Description */
.desc {
    margin-top: 20px;
    color: #94a3b8;
    line-height: 1.6;
}

/* Actions */
.actions {
    margin-top: 30px;
    display: flex;
    gap: 15px;
}

.btn {
    padding: 12px 20px;
    border-radius: 10px;
    text-decoration: none;
    font-weight: 600;
}

.primary {
    background: #06b6d4;
    color: white;
}

.secondary {
    border: 1px solid #334155;
    color: white;
}

/* Card */
.card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 20px;
    padding: 30px;
    backdrop-filter: blur(10px);
}

.card-inner h3 {
    font-size: 22px;
    margin-bottom: 20px;
}

.card-inner ul {
    list-style: none;
    padding: 0;
    color: #cbd5e1;
}

.card-inner li {
    margin-bottom: 10px;
}

/* Stats */
.stats {
    display: flex;
    justify-content: space-between;
    margin-top: 30px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    padding-top: 20px;
}

.stats h4 {
    font-size: 20px;
    color: #06b6d4;
}

.cv-btn {
    background: transparent;
    border: 1px solid rgba(6, 182, 212, 0.4);
    color: #06b6d4;
}

.cv-btn:hover {
    background: rgba(6, 182, 212, 0.1);
}

/* Responsive */
@media (max-width: 900px) {
    .container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .actions {
        justify-content: center;
    }
}
</style>