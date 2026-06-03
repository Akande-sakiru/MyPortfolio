<template>
    <section id="projects" class="projects">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>Featured Projects</h2>

                <p>
                    Real systems I’ve designed and developed from scratch,
                    focusing on scalability, automation, and real-world impact.
                </p>

            </div>

            <!-- Grid -->
            <div class="grid">

                <div v-for="(project, index) in projects" :key="index" class="card" data-aos="zoom-in">

                    <div class="type">
                        {{ project.type }}
                    </div>

                    <h3>{{ project.title }}</h3>

                    <h4>{{ project.subtitle }}</h4>

                    <p class="desc">
                        {{ project.description }}
                    </p>

                    <!-- Stack -->
                    <div class="stack">
                        <span v-for="tech in project.stack" :key="tech">
                            {{ tech }}
                        </span>
                    </div>

                    <!-- Impact -->
                    <div class="impact">
                        <strong>Impact:</strong> {{ project.impact }}
                    </div>

                </div>

            </div>

        </div>

    </section>
</template>

<script setup>
import projects from "../data/projects";
</script>

<style scoped>
.projects {
    padding: 120px 0;
    background: #020617;
    color: white;
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 0 24px;
}

/* Header */
.header {
    text-align: center;
    margin-bottom: 60px;
}

.header h2 {
    font-size: 36px;
    font-weight: 800;
    color: #06b6d4;
}

.header p {
    color: #94a3b8;
    max-width: 650px;
    margin: 10px auto 0;
}

/* Grid */
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
}

/* Card */
.card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    padding: 25px;
    backdrop-filter: blur(10px);
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-5px);
    border-color: rgba(6, 182, 212, 0.4);
}

/* Type badge */
.type {
    display: inline-block;
    font-size: 12px;
    color: #06b6d4;
    margin-bottom: 10px;
    background: rgba(6, 182, 212, 0.1);
    padding: 4px 10px;
    border-radius: 999px;
}

/* Text */
h3 {
    font-size: 20px;
    margin-bottom: 5px;
}

h4 {
    font-size: 14px;
    color: #94a3b8;
    margin-bottom: 15px;
}

.desc {
    font-size: 14px;
    color: #cbd5e1;
    line-height: 1.6;
}

/* Stack */
.stack {
    margin-top: 15px;
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}

.stack span {
    font-size: 12px;
    padding: 4px 8px;
    border-radius: 6px;
    background: rgba(255, 255, 255, 0.05);
    color: #cbd5e1;
}

/* Impact */
.impact {
    margin-top: 15px;
    font-size: 13px;
    color: #94a3b8;
}

/* Responsive */
@media (max-width: 1000px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 650px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
</style>