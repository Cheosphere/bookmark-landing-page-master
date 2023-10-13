<script setup>
import { ref } from 'vue'
import Swal from 'sweetalert2';

const email = ref('')
const emailRegex = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/
const isValidEmail = ref(true);
const isError = ref(false)
const isIcon = ref(false)

const validateEmail = () => {
    isValidEmail.value = emailRegex.test(email.value);
    if (!isValidEmail.value) {
        isError.value = true
        isIcon.value = true
    } else {
        isError.value = false
        isIcon.value = false
        Swal.fire({
            title: '¡Success!',
            text: 'The email has been entered correctly',
            icon: 'success',
        })
        email.value = ''
    }

}

</script>

<template>
    <section class="newsletter">
        <p class="newsletter-data">35,000+ ALREADY JOINED</p>
        <h2 class="newsletter-title">Stay up-to-date with what we’re doing</h2>
        <form action="#" @submit.prevent="onSubmit">
            <input v-model="email" type="text" placeholder="Enter your email address">
            <img class="error-icon" :class="{ icon: isIcon }" src="../assets/images/icon-error.svg" alt="icon error">
            <button @click="validateEmail" type="submit">Contact Us</button>
            <div class="error-email" :class="{ error: isError }">
                <p v-if="!isValidEmail">Whoops, make sure it's an email</p>
            </div>
        </form>
    </section>
</template>

<style scoped>
.newsletter {
    width: 100%;
    height: 360px;
    margin-top: 9.4rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: var(--soft-blue);
    color: #fff;
}

.newsletter-data {
    margin-top: 4.35rem;
    margin-left: .45rem;
    font-size: .8rem;
    letter-spacing: .33rem;
}

.newsletter-title {
    max-width: 450px;
    margin-top: 2.3rem;
    font-weight: 400;
    font-size: 2rem;
    line-height: 2.5rem;
    letter-spacing: .02rem;
    text-align: center;
}

form {
    margin-top: 2.2rem;
    position: relative;
}

input {
    width: 300px;
    height: 48px;
    margin-right: 1rem;
    padding-left: 1.3rem;
    border-radius: 6px;
    border: none;
    position: relative;
    z-index: 10;
}

input::placeholder {
    font-size: .9rem;
    color: var(--grayish-blue);
    opacity: .35;
}

input:focus {
    outline: 2px solid var(--soft-red);
    outline-offset: -2px;
}

button {
    width: 126px;
    height: 48px;
    border-radius: 6px;
    color: #fff;
    background-color: var(--soft-red);
    outline: 2px solid hsla(0, 94%, 66%, 0);
    outline-offset: -2px;
    border: none;
    letter-spacing: .05rem;
    cursor: pointer;
    transition: .3s;
}

button:hover {
    color: var(--soft-red);
    background-color: #fff;
    outline: 2px solid hsla(0, 94%, 66%, 100);
}

.error-email {
    width: 300px;
    padding: .8rem 1rem .5rem 1rem;
    position: relative;
    bottom: 2.5rem;
    font-size: .8rem;
    font-style: italic;
    background-color: transparent;
    border-radius: 0 0 5px 5px;
    transition: .3s;
}

.error {
    bottom: .3rem;
    background-color: var(--soft-red);
}

.error-icon {
    position: absolute;
    top: 14px;
    right: 150px;
    z-index: 10;
    opacity: 0;
    transition: .3s;
}

.icon {
    opacity: 1;
}

/* MEDIA QUERY */
@media screen and (max-width: 540px) {
    .newsletter {
        height: fit-content;
        padding: 3rem .5rem;
    }

    .newsletter-data,
    .newsletter-title {
        margin: 0 0 .7rem 0;
    }

    form {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    input,
    button {
        width: 90%;
        margin: 0 0 1rem 0;
    }

    input {
        order: 0;
    }

    button {
        order: 3;
    }

    .error {
        bottom: 1.3rem;
    }

    .error-email {
        width: 90%;
        order: 1;
    }

    .error-icon {
        right: 46px;
    }
}

@media screen and (max-width: 374px) {
    .newsletter-title {
        font-size: 1.8rem;
    }
}</style>