<template>
    <section id="experience" class="experience">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>Professional Experience</h2>

                <p>
                    Real-world systems I’ve built and contributed to,
                    focusing on scalability, automation, and impact.
                </p>

            </div>

            <!-- Timeline -->
            <div class="timeline">

                <div v-for="(item, index) in experience" :key="index" class="card" data-aos="fade-up">

                    <!-- Left Side -->
                    <div class="left">

                        <h3>{{ item.role }}</h3>
                        <h4>{{ item.company }}</h4>
                        <span>{{ item.period }}</span>

                        <p class="desc">
                            {{ item.description }}
                        </p>

                    </div>

                    <!-- Right Side -->
                    <div class="right">

                        <ul>
                            <li v-for="(h, i) in item.highlights" :key="i">
                                ✔ {{ h }}
                            </li>
                        </ul>

                    </div>

                </div>

            </div>

        </div>

    </section>
</template>

<script setup>
import experience from "../data/experience";
</script>

<style scoped>
.experience {
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
    max-width: 600px;
    margin: 10px auto 0;
}

/* Timeline Cards */
.card {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    padding: 30px;
    margin-bottom: 20px;
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    backdrop-filter: blur(10px);
}

/* Left */
.left h3 {
    color: #06b6d4;
    font-size: 22px;
}

.left h4 {
    margin-top: 5px;
    color: #e2e8f0;
}

.left span {
    font-size: 13px;
    color: #94a3b8;
}

.desc {
    margin-top: 15px;
    color: #94a3b8;
    line-height: 1.6;
}

/* Right */
.right ul {
    list-style: none;
    padding: 0;
}

.right li {
    padding: 6px 0;
    color: #cbd5e1;
    font-size: 14px;
}

/* Responsive */
@media (max-width: 900px) {
    .card {
        grid-template-columns: 1fr;
    }
}
</style>