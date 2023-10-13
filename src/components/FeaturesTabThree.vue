<script setup>
</script>

<template>
    <section class="sb-container">
        <figure class="sb-image">
            <img src="../assets/images/illustration-features-tab-3.svg" alt="illustration simple bookmarking">
            <div class="bg"></div>
        </figure>
        <div class="sb-info">
            <h2 class="sb-info-title">Share your bookmarks</h2>
            <p class="sb-info-text">
                Easily share your bookmarks and collections with others. Create a shareable
                link that you can send at the click of a button.
            </p>
            <button class="btn">More Info</button>
        </div>
    </section>
</template>

<style scoped>
.sb-container {
    width: 100%;
    margin-top: 4.4rem;
    margin-left: .3rem;
    display: flex;
}

.sb-image {
    margin-left: -.05rem;
    position: relative;
}

.bg {
    width: 100vw;
    height: 352px;
    position: absolute;
    bottom: -3.2rem;
    right: 2.8rem;
    background-color: var(--soft-blue);
    z-index: -10;
    border-radius: 352px;
}

.sb-info {
    padding-left: 13.82rem;
    padding-top: 4rem;
}

.sb-info-title {
    font-size: 1.9rem;
    font-weight: 500;
    color: var(--very-dark-blue);
}

.sb-info-text {
    margin-top: 1.5rem;
    color: var(--grayish-blue);
    font-weight: 300;
    font-size: 1.1rem;
    line-height: 1.75rem;
    letter-spacing: .027rem;
}

.btn {
    margin-top: 2rem;
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
@media screen and (max-width: 1240px) {
    .sb-container {
        margin-left: 0;
    }

    .sb-info {
        padding-left: 8rem;
    }

    .sb-image {
        transform: scale(.92);
    }

}

@media screen and (max-width: 1080px) {
    .sb-container {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .sb-info {
        padding: 5.95rem 0 0 0;
    }

    .sb-image {
        transform: none;
    }

    .bg {
        width: 2000px;
    }
}

@media screen and (max-width: 640px) {
    .sb-image {
        transform: scale(.9);
    }

    .bg {
        bottom: -3.1rem;
    }
}

@media screen and (max-width: 540px) {
    .sb-info {
        padding: 3.95rem 0 0 0;
    }

    .sb-image {
        transform: scale(.7);
    }

    .bg {
        bottom: -2.8rem;
    }
}

@media screen and (max-width: 440px) {
    .sb-info {
        padding: 1.95rem 0 0 0;
    }

    .sb-info-text {
        font-size: 1rem;
    }

    .sb-image {
        transform: scale(.6);
    }

    .bg {
        bottom: -2.5rem;
    }
}

@media screen and (max-width: 374px) {
    .sb-image {
        transform: scale(.55);
    }

    .bg {
        bottom: -2.35rem;
    }
}</style>