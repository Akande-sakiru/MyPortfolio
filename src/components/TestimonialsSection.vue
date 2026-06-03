<template>
    <section id="testimonials" class="testimonials">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>What People Say</h2>

                <p>
                    Feedback from systems and platforms I’ve built and contributed to.
                </p>

            </div>

            <!-- Grid -->
            <div class="grid">

                <div v-for="(item, index) in testimonials" :key="index" class="card" data-aos="zoom-in">

                    <p class="message">
                        "{{ item.message }}"
                    </p>

                    <div class="info">

                        <div class="avatar">
                            {{ item.name.charAt(0) }}
                        </div>

                        <div>
                            <h4>{{ item.name }}</h4>
                            <span>{{ item.role }}</span>
                        </div>

                    </div>

                </div>

            </div>

        </div>

    </section>
</template>

<script setup>
import testimonials from "../data/testimonials";
</script>

<style scoped>
.testimonials {
    padding: 120px 0;
    background: #020617;
    color: white;
}

.container {
    max-width: 1100px;
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

/* Message */
.message {
    color: #cbd5e1;
    font-size: 14px;
    line-height: 1.6;
    margin-bottom: 20px;
}

/* Info */
.info {
    display: flex;
    align-items: center;
    gap: 12px;
}

/* Avatar */
.avatar {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: #06b6d4;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}

/* Text */
h4 {
    margin: 0;
    font-size: 14px;
}

span {
    font-size: 12px;
    color: #94a3b8;
}

/* Responsive */
@media (max-width: 900px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
</style>