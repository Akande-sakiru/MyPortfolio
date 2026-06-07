<template>
    <footer class="footer">

        <div class="container">

            <div class="grid">

                <!-- Brand -->
                <div class="brand" data-aos="fade-up">

                    <h2>Sakiru<span>.</span></h2>

                    <p>
                        Full Stack Software Engineer specializing in building
                        scalable ERP systems, SaaS platforms, and enterprise applications.
                    </p>

                </div>

                <!-- Quick Links -->
                <div class="links" data-aos="fade-up">

                    <h3>Quick Links</h3>

                    <ul>
                        <li><a href="#about">About</a></li>
                        <li><a href="#skills">Skills</a></li>
                        <li><a href="#experience">Experience</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>

                </div>

                <!-- Services -->
                <div class="services" data-aos="fade-up">

                    <h3>Services</h3>

                    <ul>
                        <li>Web Development</li>
                        <li>ERP Systems</li>
                        <li>SaaS Development</li>
                        <li>API Architecture</li>
                        <li>System Design</li>
                    </ul>

                </div>

                <!-- Contact -->
                <div class="contact" data-aos="fade-up">

                    <h3>Contact</h3>
                    <p>Email: oluwadamilareakande411@gmail.com</p>
                    <p>Lagos, Nigeria</p>

                    <div class="socials">

                        <a href="https://github.com/Akande-sakiru" target="_blank">GitHub</a>
                        <a href="https://linkedin.com/in/Akande-sakiru" target="_blank">LinkedIn</a>
                        <a href="https://wa.me/2348169453935" target="_blank">WhatsApp</a>

                    </div>

                </div>

            </div>

            <!-- Bottom -->
            <div class="bottom">

                <p>
                    © {{ new Date().getFullYear() }} Sakiru Akande. All rights reserved.
                </p>

                <p class="tag">
                    Built with Vue 3 • Laravel Mindset • SaaS Architecture Thinking
                </p>

            </div>

        </div>

    </footer>
</template>

<style scoped>
.footer {
    background: #020617;
    color: white;
    padding: 80px 0 30px;
    border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 0 24px;
}

/* Grid */
.grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 40px;
    margin-bottom: 60px;
}

/* Brand */
.brand h2 {
    font-size: 28px;
    font-weight: 800;
}

.brand span {
    color: #06b6d4;
}

.brand p {
    margin-top: 10px;
    color: #94a3b8;
    line-height: 1.6;
    font-size: 14px;
}

/* Sections */
h3 {
    color: #06b6d4;
    margin-bottom: 15px;
    font-size: 16px;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    margin-bottom: 8px;
    font-size: 14px;
    color: #cbd5e1;
}

a {
    color: #cbd5e1;
    text-decoration: none;
}

a:hover {
    color: #06b6d4;
}

/* Socials */
.socials {
    margin-top: 10px;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

/* Bottom */
.bottom {
    border-top: 1px solid rgba(255, 255, 255, 0.05);
    padding-top: 20px;
    text-align: center;
}

.bottom p {
    font-size: 13px;
    color: #94a3b8;
}

.tag {
    margin-top: 5px;
    color: #06b6d4;
}

/* Responsive */
@media (max-width: 900px) {
    .grid {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 600px) {
    .grid {
        grid-template-columns: 1fr;
        text-align: center;
    }
}
</style>