<template>
    <div class="container">
        <div class="menu"><Menu /></div>
        <div class="header">
            <div><Header /></div>
            <div class="homefeed"><HomeFeed /></div>
        </div>
    </div>
</template>

<script setup>
import Menu from './components/Menu.vue';
import Header from './components/Header.vue';
import HomeFeed from './components/HomeFeed.vue';
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
}

.container {
    display: flex;
}
.menu {
    flex-basis: 15%;
}

.header {
    flex-basis: 85%;
}

.homefeed {
    position: absolute;
    top: 0;
    z-index: -1;
}

/* Media Query */
@media only screen and (max-width: 768px) {
    .menu {
        display: none;
    }
    .header {
        flex-basis: 100%;
    }
}
</style>
