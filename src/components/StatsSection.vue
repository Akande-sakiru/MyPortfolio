<template>
    <section id="stats" class="stats">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>Impact & Experience</h2>

                <p>
                    A quick overview of my professional journey and the systems I’ve built.
                </p>

            </div>

            <!-- Stats Grid -->
            <div class="grid">

                <div class="card" data-aos="zoom-in">
                    <h3>5+</h3>
                    <p>Years of Experience</p>
                </div>

                <div class="card" data-aos="zoom-in">
                    <h3>20+</h3>
                    <p>Projects Completed</p>
                </div>

                <div class="card" data-aos="zoom-in">
                    <h3>10+</h3>
                    <p>Systems Built</p>
                </div>

                <div class="card" data-aos="zoom-in">
                    <h3>100K+</h3>
                    <p>Users Impacted</p>
                </div>

            </div>

        </div>

    </section>
</template>

<style scoped>
.stats {
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
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
}

/* Card */
.card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    padding: 30px;
    text-align: center;
    backdrop-filter: blur(10px);
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-5px);
    border-color: rgba(6, 182, 212, 0.4);
}

/* Numbers */
.card h3 {
    font-size: 32px;
    color: #06b6d4;
    margin-bottom: 10px;
}

.card p {
    color: #94a3b8;
    font-size: 14px;
}

/* Responsive */
@media (max-width: 900px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 500px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
</style>