<template>
    <section id="contact" class="contact">

        <div class="container">

            <!-- Header -->
            <div class="header" data-aos="fade-up">

                <h2>Let’s Build Something Great</h2>

                <p>
                    Have a project, idea, or opportunity?
                    I’m available for freelance, contract, and full-time roles.
                </p>

            </div>

            <div class="grid">

                <!-- Left: Contact Info -->
                <div class="info" data-aos="fade-right">

                    <h3>Get in Touch</h3>

                    <p>
                        I typically respond within 24 hours.
                    </p>

                    <div class="contact-box">

                        <p><strong>Email:</strong> oluwadamilareakande411@gmail.com</p>
                        <p><strong>Location:</strong> Lagos, Nigeria</p>

                    </div>

                    <a href="https://wa.me/2348169453935" target="_blank" class="whatsapp">
                        Chat on WhatsApp
                    </a>

                </div>

                <!-- Right: Form -->
                <form class="form" @submit.prevent="sendEmail" data-aos="fade-left">

                    <input v-model="name" type="text" placeholder="Your Name" required />

                    <input v-model="email" type="email" placeholder="Your Email" required />

                    <textarea v-model="message" placeholder="Your Message" rows="6" required></textarea>

                    <button type="submit">
                        Send Message
                    </button>

                    <p v-if="success" class="success">
                        Message sent successfully 🚀
                    </p>

                </form>

            </div>

        </div>

    </section>
</template>

<script setup>
import { ref } from "vue";
import emailjs from "@emailjs/browser";

const name = ref("");
const email = ref("");
const message = ref("");
const success = ref(false);

const sendEmail = async () => {
    try {
        await emailjs.send(
            "SERVICE_ID",
            "TEMPLATE_ID",
            {
                name: name.value,
                email: email.value,
                message: message.value,
            },
            "PUBLIC_KEY"
        );

        success.value = true;

        name.value = "";
        email.value = "";
        message.value = "";

        setTimeout(() => {
            success.value = false;
        }, 3000);

    } catch (error) {
        console.log(error);
    }
};
</script>

<style scoped>
.contact {
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
    grid-template-columns: 1fr 1fr;
    gap: 40px;
}

/* Info */
.info h3 {
    font-size: 24px;
    margin-bottom: 10px;
}

.info p {
    color: #94a3b8;
    margin-bottom: 20px;
}

.contact-box {
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.08);
    padding: 20px;
    border-radius: 12px;
    margin-bottom: 20px;
}

.whatsapp {
    display: inline-block;
    background: #06b6d4;
    color: white;
    padding: 10px 18px;
    border-radius: 10px;
    text-decoration: none;
    font-weight: 600;
}

/* Form */
.form {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

input,
textarea {
    padding: 12px;
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    background: rgba(255, 255, 255, 0.03);
    color: white;
    outline: none;
}

button {
    padding: 12px;
    background: #06b6d4;
    color: white;
    border: none;
    border-radius: 10px;
    font-weight: 600;
    cursor: pointer;
}

/* Success message */
.success {
    color: #22c55e;
    font-size: 14px;
}

/* Responsive */
@media (max-width: 900px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
</style>