<template>
    <section id="about" class="about">

        <div class="container">

            <!-- Left Side (Text) -->
            <div class="left" data-aos="fade-right">

                <h2 class="section-title">
                    About Me
                </h2>

                <h3 class="subtitle">
                    Building scalable systems for education and enterprise
                </h3>

                <p class="text">
                    I am a Full Stack Software Engineer specializing in building
                    <strong>enterprise-grade applications</strong>,
                    <strong>ERP systems</strong>, and
                    <strong>SaaS platforms</strong>.
                </p>

                <p class="text">
                    Over the years, I have designed and developed systems such as
                    <strong>EduTAMS</strong> (Student Information System) and
                    <strong>ElectaGN</strong> (E-Voting SaaS), helping institutions
                    digitize and automate critical operations.
                </p>

                <!-- Key Highlights -->
                <div class="highlights">

                    <div class="card">
                        <h4>ERP Systems</h4>
                        <p>Student & enterprise management platforms</p>
                    </div>

                    <div class="card">
                        <h4>SaaS Platforms</h4>
                        <p>Scalable multi-user web applications</p>
                    </div>

                    <div class="card">
                        <h4>API Architecture</h4>
                        <p>Secure and scalable backend systems</p>
                    </div>

                </div>

            </div>

            <!-- Right Side (Visual / Stats) -->
            <div class="right" data-aos="fade-left">

                <div class="profile-card">

                    <div class="avatar">
                        SA
                    </div>

                    <h3>Sakiru Akande</h3>
                    <p>Full Stack Software Engineer</p>

                    <div class="experience">
                        <div>
                            <h4>3+</h4>
                            <span>Years Experience</span>
                        </div>

                        <div>
                            <h4>10+</h4>
                            <span>Projects</span>
                        </div>

                        <div>
                            <h4>6+</h4>
                            <span>Systems Built</span>
                        </div>
                    </div>

                </div>

                <!-- Floating Info Cards -->
                <div class="floating-card card-1">
                    ✔ Laravel Expert
                </div>

                <div class="floating-card card-2">
                    ✔ Vue.js Specialist
                </div>

                <div class="floating-card card-3">
                    ✔ SaaS Architect
                </div>

            </div>

        </div>

    </section>
</template>


<style scoped>
.about {
    padding: 120px 0;
    background: #020617;
    color: white;
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 0 24px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
}

/* Section Title */
.section-title {
    font-size: 36px;
    font-weight: 800;
    color: #06b6d4;
}

.subtitle {
    font-size: 22px;
    margin-top: 10px;
    color: #e2e8f0;
}

.text {
    margin-top: 20px;
    color: #94a3b8;
    line-height: 1.7;
}

/* Highlights */
.highlights {
    margin-top: 40px;
    display: grid;
    gap: 15px;
}

.highlights .card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    padding: 20px;
    border-radius: 12px;
}

.highlights h4 {
    color: #06b6d4;
    margin-bottom: 5px;
}

/* Right Side */
.right {
    position: relative;
}

/* Profile Card */
.profile-card {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 20px;
    padding: 40px;
    text-align: center;
    backdrop-filter: blur(10px);
}

.avatar {
    width: 80px;
    height: 80px;
    margin: auto;
    border-radius: 50%;
    background: #06b6d4;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 24px;
    margin-bottom: 15px;
}

.experience {
    display: flex;
    justify-content: space-between;
    margin-top: 30px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    padding-top: 20px;
}

.experience h4 {
    color: #06b6d4;
    font-size: 20px;
}

/* Floating Cards */
.floating-card {
    position: absolute;
    background: rgba(6, 182, 212, 0.1);
    border: 1px solid rgba(6, 182, 212, 0.3);
    padding: 10px 14px;
    border-radius: 999px;
    font-size: 12px;
    color: #06b6d4;
    backdrop-filter: blur(10px);
}

.card-1 {
    top: 20px;
    left: -20px;
}

.card-2 {
    bottom: 60px;
    right: -50px;
}

.card-3 {
    top: 120px;
    right: -40px;
}

/* Responsive */
@media (max-width: 900px) {
    .container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .floating-card {
        display: none;
    }
}
</style>