<script setup></script>

<template>
    <section class="download">
        <div class="download-info">
            <h2 class="download-info-title">Download the extension</h2>
            <p class="download-info-text">
                We’ve got more browsers in the pipeline. Please do let us know if you’ve
                got a favourite you’d like us to prioritize.
            </p>
        </div>
        <div class="download-cards">
            <div class="chrome-card">
                <figure class="chrome-card-logo">
                    <img src="../assets/images/logo-chrome.svg" alt="chrome logo">
                </figure>
                <h3 class="chrome-card-title">Add to Chrome</h3>
                <p class="chrome-card-version">Minimum version 62</p>
                <figure class="chrome-card-dots">
                    <img src="../assets/images/bg-dots.svg" alt="dots image">
                </figure>
                <button class="chrome-card-btn">Add & Install Extension</button>
            </div>
            <div class="firefox-card">
                <figure class="firefox-card-logo">
                    <img src="../assets/images/logo-firefox.svg" alt="chrome logo">
                </figure>
                <h2 class="firefox-card-title">Add to Firefox</h2>
                <p class="firefox-card-version">Minimum version 55</p>
                <figure>
                    <img class="firefox-card-dots" src="../assets/images/bg-dots.svg" alt="dots image">
                </figure>
                <button class="firefox-card-btn">Add & Install Extension</button>
            </div>
            <div class="opera-card">
                <figure class="opera-card-logo">
                    <img src="../assets/images/logo-opera.svg" alt="chrome logo">
                </figure>
                <h2 class="opera-card-title">Add to Opera</h2>
                <p class="opera-card-version">Minimum version 46</p>
                <figure class="opera-card-dots">
                    <img src="../assets/images/bg-dots.svg" alt="dots image">
                </figure>
                <button class="opera-card-btn">Add & Install Extension</button>
            </div>
        </div>
    </section>
</template>

<style scoped>
.download {
    padding-top: 10.7rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.download-info {
    display: flex;
    flex-direction: column;
    text-align: center;
}

.download-info-title {
    font-size: 1.98rem;
    font-weight: 500;
    letter-spacing: .005rem;
    color: var(--very-dark-blue);
}

.download-info-text {
    max-width: 545px;
    margin-top: 1.46rem;
    color: var(--grayish-blue);
    font-weight: 300;
    font-size: 1.1rem;
    line-height: 1.75rem;
    letter-spacing: .027rem;
}

.download-cards {
    width: 100%;
    display: flex;
    justify-content: center;
}

/* CARDS STYLES */
.chrome-card,
.firefox-card,
.opera-card {
    width: 280px;
    height: 362px;
    margin-top: 3.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    border-radius: 1rem;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.08);
    transition: .3s;

}

.chrome-card-logo,
.firefox-card-logo {
    margin-top: 2.55rem;
}

.chrome-card-title,
.firefox-card-title,
.opera-card-title {
    margin-top: 1.8rem;
    font-size: 1.2rem;
    font-weight: 500;
    letter-spacing: .04rem;
}

.chrome-card-version,
.firefox-card-version,
.opera-card-version {
    margin-top: .65rem;
    color: var(--grayish-blue);
    font-size: .95rem;
    font-weight: 300;
}

.chrome-card-dots {
    margin-top: 1.6rem;
}

.firefox-card-dots {
    margin-top: 2.3rem;
}

.opera-card-dots {
    margin-top: 1.6rem;
}

.chrome-card-btn,
.firefox-card-btn,
.opera-card-btn {
    margin-top: 1.25rem;
    padding: 1rem 2.2rem;
    background-color: var(--soft-blue);
    color: #fff;
    border: none;
    border-radius: 5px;
    letter-spacing: .045rem;
    font-weight: 500;
    box-shadow: 0 8px 12px -5px rgba(0, 0, 0, 0.16);
    outline: 2px solid hsla(231, 69%, 60%, 0);
    outline-offset: -2px;
    cursor: pointer;
    transition: .3s;
}

.chrome-card-btn:hover,
.firefox-card-btn:hover,
.opera-card-btn:hover {
    color: var(--soft-blue);
    background-color: #fff;
    outline: 2px solid hsla(231, 69%, 60%, 100);
}

.opera-card-btn {
    padding: 1rem 2.15rem;
}

.firefox-card {
    margin: 6rem 2.1rem 0 2.15rem;
}

.opera-card {
    width: 280px;
    margin-top: 8.5rem;
    position: relative;
    left: 3px;
}

.opera-card-logo {
    margin-top: 2.55rem;
}

/* MEDIA QUERY */
@media screen and (max-width: 960px) {
    .download-cards {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .chrome-card,
    .firefox-card,
    .opera-card {
        margin-top: 2rem;
    }

    .chrome-card {
        margin-top: 3rem;
    }
}

@media screen and (max-width: 440px) {
    .download {
        padding-top: 5rem;
    }

    .download-info-title {
        font-size: 1.7rem;
    }

    .download-info-text {
        font-size: 1rem;
    }
}
</style>