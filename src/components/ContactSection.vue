<template>
    <section id="contact">

        <form @submit.prevent="sendMail">

            <input v-model="name" placeholder="Name" />

            <input v-model="email" placeholder="Email" />

            <textarea v-model="message"></textarea>

            <button>
                Send Message
            </button>

        </form>

    </section>
</template>

<script setup>
import emailjs from "@emailjs/browser";

const sendMail = () => {
    emailjs.send(
        "SERVICE_ID",
        "TEMPLATE_ID",
        {
            name,
            email,
            message,
        },
        "PUBLIC_KEY"
    );
};
</script>