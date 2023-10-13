<script setup>
</script>

<template>
    <section class="sb-container">
        <figure class="sb-image">
            <img src="../assets/images/illustration-features-tab-1.svg" alt="illustration simple bookmarking">
            <div class="bg"></div>
        </figure>
        <div class="sb-info">
            <h2 class="sb-info-title">Bookmark in one click</h2>
            <p class="sb-info-text">
                Organize your bookmarks however you like. Our simple drag-and-drop interface
                gives you complete control over how you manage your favourite sites.
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
    bottom: -5.3rem;
    right: 4.05rem;
    background-color: var(--soft-blue);
    z-index: -10;
    border-radius: 352px;
}

.sb-info {
    padding-left: 7.82rem;
    padding-top: 4rem;
}

.sb-info-title {
    font-size: 1.96rem;
    color: var(--very-dark-blue);
    font-weight: 500;
    letter-spacing: 0.015rem;
}

.sb-info-text {
    margin-top: 1.45rem;
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
        padding-left: 5rem;
    }

    .sb-image {
        margin: 0;
        transform: scale(.9);
    }

    .sb-info {
        padding-left: 2rem;
    }
}

@media screen and (max-width: 1080px) {
    .sb-container {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .sb-info {
        padding: 8.05rem 0 0 0;
    }

    .sb-image {
        transform: none;
    }

    .bg {
        width: 2000px;
        bottom: -5.35rem;
    }

}

@media screen and (max-width: 640px) {
    .sb-image {
        transform: scale(.9);
    }
}

@media screen and (max-width: 540px) {
    .sb-image {
        transform: scale(.7);
    }

    .sb-info {
        padding: 6rem 0 0 0;
    }
}

@media screen and (max-width: 440px) {
    .sb-image {
        transform: scale(.6);
    }

    .sb-info {
        padding: 4rem 0 0 0;
    }

    .sb-info-title {
        font-size: 1.7rem;
    }

    .sb-info-text {
        font-size: 1rem;
    }
}

@media screen and (max-width: 374px) {
    .sb-image {
        transform: scale(.55);
    }
}</style>