<script setup>
import { ref } from 'vue'
import FeaturesTabOne from './FeaturesTabOne.vue'
import FeaturesTabTwo from './FeaturesTabTwo.vue'
import FeaturesTabThree from './FeaturesTabThree.vue'

let option = ref(1)

const selectedItem = ref(0)

const toggle = (index) => {

    if (index === 0) {
        option.value = 1
    }
    if (index === 1) {
        option.value = 2
    }
    if (index === 2) {
        option.value = 3
    }

    selectedItem.value = index
}

</script>

<template>
    <section class="features">
        <div class="features-info">
            <h2 class="features-title">Features</h2>
            <p class="features-text">
                Our aim is to make it quick and easy for you to access your favourite websites.
                Your bookmarks sync between your devices so you can access them on the go.
            </p>
        </div>
        <div class="features-tabs">
            <nav>
                <ul>
                    <li><a @click="toggle(0)" :class="{ 'selected-item': selectedItem === 0 }" href="javascript:;">Simple
                            Bookmarking</a></li>
                    <li><a @click="toggle(1)" :class="{ 'selected-item': selectedItem === 1 }" href="javascript:;">Speedy
                            Searching</a></li>
                    <li><a @click="toggle(2)" :class="{ 'selected-item': selectedItem === 2 }" href="javascript:;">Easy
                            Sharing</a></li>
                </ul>
                <!-- <hr> -->
            </nav>
        </div>
        <div class="features-content" v-show="option === 1">
            <FeaturesTabOne />
        </div>
        <div class="features-content" v-show="option === 2">
            <FeaturesTabTwo />
        </div>
        <div class="features-content" v-show="option === 3">
            <FeaturesTabThree />
        </div>
    </section>
</template>

<style scoped>
.features {
    min-height: 758px;
    margin-top: 7rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.features-info {
    width: 100%;
    max-width: 540px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.features-title {
    font-size: 2rem;
    font-weight: 500;
    color: var(--very-dark-blue);
}

.features-text {
    margin-top: 1.45rem;
    color: var(--grayish-blue);
    font-weight: 300;
    font-size: 1.1rem;
    line-height: 1.75rem;
    letter-spacing: .027rem;
}

.features-tabs {
    width: 100%;
    max-width: 730px;
    margin-top: 4.44rem;
    display: flex;
    justify-content: center;
    z-index: 10;
}

nav {
    width: 100%;
}

ul {
    display: flex;
}

li {
    width: 100%;
    display: flex;
    justify-content: center;
    border-bottom: 1px solid rgba(211, 211, 211, 0.6);
}

a {
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 0 0 1.62rem;
    color: var(--grayish-blue);
    letter-spacing: .03rem;
    border-bottom: 4px solid #fff;
    transition: .2s;
}

a:hover {
    color: var(--soft-red);
}

.selected-item {
    color: var(--very-dark-blue);
    border-bottom: 4px solid var(--soft-red);
}

.features-content {
    width: 100%;
    margin-top: .1rem;
    transition: .3s;
}

/* MEDIA QUERY */
@media screen and (max-width: 1080px) {
    .features-tabs {
        width: 80%;
        max-width: none;
    }

    ul {
        flex-direction: column;
    }

    li:first-child {
        border-top: 1px solid rgba(211, 211, 211, 0.6);
    }

    a {
        width: 160px;
        padding: 1rem;
    }
}

@media screen and (max-width: 540px) {
    .features-content {
        position: relative;
        bottom: 2rem;
    }

    .features-tabs {
        width: 100%;
    }
}

@media screen and (max-width: 440px) {
    .features {
        margin-top: 2rem;
    }

    .features-content {
        bottom: 4rem;
    }

    .features-title {
        font-size: 1.7rem;
    }

    .features-text {
        font-size: 1rem;
        line-height: 1.75rem;
        letter-spacing: .027rem;
    }
}</style>