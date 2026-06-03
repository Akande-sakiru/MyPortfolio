<template>
    <section id="skills" class="skills">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>Skills & Expertise</h2>

                <p>
                    My technical toolkit for building scalable systems,
                    enterprise applications, and modern SaaS platforms.
                </p>

            </div>

            <!-- Skills Grid -->
            <div class="grid">

                <div v-for="(skill, index) in skills" :key="index" class="card" data-aos="zoom-in">

                    <h3>{{ skill.category }}</h3>

                    <ul>
                        <li v-for="item in skill.items" :key="item">
                            {{ item }}
                        </li>
                    </ul>

                </div>

            </div>

        </div>

    </section>
</template>

<script setup>
import skills from "../data/skills";
</script>

<style scoped>
.skills {
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
    margin-top: 10px;
    color: #94a3b8;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
}

/* Grid */
.grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
}

/* Card */
.card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    padding: 25px;
    border-radius: 16px;
    backdrop-filter: blur(10px);
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-5px);
    border-color: rgba(6, 182, 212, 0.4);
}

.card h3 {
    color: #06b6d4;
    margin-bottom: 15px;
}

/* List */
ul {
    list-style: none;
    padding: 0;
}

li {
    padding: 6px 0;
    color: #cbd5e1;
    font-size: 14px;
}

/* Responsive */
@media (max-width: 1000px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 600px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
</style>