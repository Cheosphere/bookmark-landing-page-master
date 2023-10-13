<script setup>
import { ref } from 'vue'

const questions = ref([
    {
        title: 'What is Bookmark?',
        answer: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo eget ultricies fringilla. Phasellus blandit ipsum quis quam ornare mattis.',
        isOpen: false
    },
    {
        title: 'How can I request a new browser?',
        answer: 'Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdiet. Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdie tVivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdiet.',
        isOpen: false
    },
    {
        title: 'Is there a mobile app?',
        answer: 'Sed consectetur quam id neque fermentum accumsan. Praesent luctus vestibulum dolor, ut condimentum urna vulputate eget. Cras in ligula quis est pharetra mattis sit amet pharetra purus. Sed sollicitudin ex et ultricies bibendum.',
        isOpen: false
    },
    {
        title: 'What about other Chromium browsers?',
        answer: 'Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi, at euismod dui. Aliquam vitae neque eget nisl gravida pellentesque non ut velit.',
        isOpen: false
    }
])

const isOpen = ref(false);

const icons = ref([
    { rotated: false },
    { rotated: false },
    { rotated: false },
    { rotated: false },
]);

const toggleAccordion = (index, id) => {
    questions.value[index].isOpen = !questions.value[index].isOpen
    icons.value[index].rotated = !icons.value[index].rotated;
}

</script>

<template>
    <section class="faq">
        <div class="faq-info">
            <h2 class="faq-info-title">Frequently Asked Questions</h2>
            <p class="faq-info-text">
                Here are some of our FAQs. If you have any other questions you’d like
                answered please feel free to email us.
            </p>
        </div>
        <div class="faq-list">
            <div class="faq-question" @click="toggleAccordion(index)" v-for="(question, index) in questions" :key="index">
                <h3 class="faq-question-title">{{ question.title }}</h3>
                <svg class="icon-arrow" :class="{ 'rotate': icons[index].rotated }" xmlns="http://www.w3.org/2000/svg"
                    width="18" height="12">
                    <path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8" />
                </svg>
                <Transition>
                    <p v-if="question.isOpen" class="faq-answer-text">{{ question.answer }}</p>
                </Transition>
            </div>
        </div>
        <button class="btn">More Info</button>
    </section>
</template>

<style scoped>
.faq {
    padding-top: 9.6rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.faq-info {
    display: flex;
    flex-direction: column;
    text-align: center;
}

.faq-info-title {
    font-size: 1.98rem;
    font-weight: 500;
    line-height: 2.8rem;
    color: var(--very-dark-blue);
}

.faq-info-text {
    max-width: 500px;
    margin-top: 1.2rem;
    color: var(--grayish-blue);
    font-weight: 300;
    font-size: 1.1rem;
    line-height: 1.75rem;
    letter-spacing: .027rem;
}

.faq-list {
    width: 100%;
    max-width: 541px;
    margin-top: 3.5rem;
    border-bottom: 1px solid lightgray;
}

.faq-question {
    width: 100%;
    padding-right: 1.48rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    border-top: 1px solid lightgray;
    cursor: pointer;
}

.faq-question:hover .faq-question-title {
    color: var(--soft-red);
}

.faq-question-title {
    margin: 1.45rem 0 1.22rem 0;
    font-size: 1.15rem;
    font-weight: 300;
    letter-spacing: .005rem;
    transition: .3s;
}

.icon-arrow {
    margin-top: 2px;
    transition: .3s;
}

.rotate {
    transform: rotate(180deg);

    &.icon-arrow path {
        stroke: var(--soft-red);
    }
}

.faq-answer-text {
    padding-bottom: 1.5rem;
    font-weight: 300;
    line-height: 2rem;
    color: var(--grayish-blue);
}

/* transition vuejs */
.v-enter-active,
.v-leave-active {
    transition: opacity 0.4s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}

.btn {
    margin-top: 3.35rem;
    padding: 1rem 1.56rem;
    background-color: var(--soft-blue);
    color: #fff;
    border: none;
    border-radius: 5px;
    letter-spacing: .03rem;
    font-weight: 500;
    box-shadow: 0 8px 12px -5px rgba(0, 0, 0, 0.16);
    outline: 2px solid hsla(231, 69%, 60%, 0);
    outline-offset: -2px;
    cursor: pointer;
    transition: .3s;
}

.btn:hover {
    color: var(--soft-blue);
    background-color: #fff;
    outline: 2px solid hsla(231, 69%, 60%, 100);
}

/* MEDIA QUERY */
@media screen and (max-width: 768px) {
    .faq-question {
        padding: 0;
    }
}

@media screen and (max-width: 440px) {
    .faq-info-title {
        font-size: 1.7rem;
    }

    .faq-info-text {
        font-size: 1rem;

    }

    .faq-question-title {
        font-size: 1rem;
    }
}

@media screen and (max-width: 374px) {

    .faq-info-text {
        font-size: 1rem;

    }

    .faq-question-title {
        font-size: 1rem;
    }

    .faq-question-title,
    .faq-answer-text {
        font-size: .9rem;
    }

}</style>