<template>
    <section id="services" class="services">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>Services I Offer</h2>

                <p>
                    I help businesses and institutions build scalable,
                    secure, and modern digital systems.
                </p>

            </div>

            <!-- Grid -->
            <div class="grid">

                <div v-for="(service, index) in services" :key="index" class="card" data-aos="zoom-in">

                    <h3>{{ service.title }}</h3>

                    <p class="desc">
                        {{ service.description }}
                    </p>

                    <ul>
                        <li v-for="point in service.points" :key="point">
                            ✔ {{ point }}
                        </li>
                    </ul>

                </div>

            </div>

        </div>

    </section>
</template>

<script setup>
import services from "../data/services";
</script>

<style scoped>
.services {
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
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
}

/* Card */
.card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    padding: 30px;
    backdrop-filter: blur(10px);
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-5px);
    border-color: rgba(6, 182, 212, 0.4);
}

/* Text */
h3 {
    color: #06b6d4;
    font-size: 20px;
    margin-bottom: 10px;
}

.desc {
    color: #94a3b8;
    font-size: 14px;
    margin-bottom: 15px;
    line-height: 1.6;
}

/* List */
ul {
    list-style: none;
    padding: 0;
}

li {
    font-size: 14px;
    color: #cbd5e1;
    padding: 5px 0;
}

/* Responsive */
@media (max-width: 900px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
</style>