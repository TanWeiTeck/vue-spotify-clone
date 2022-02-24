<template>
    <div class="header_container">
        <div class="navicons">
            <a />
            <img
                src="https://img.icons8.com/ios-glyphs/30/ffffff/back.png"
                height="20"
            />
            <img
                src="https://img.icons8.com/ios-glyphs/30/ffffff/forward.png"
                height="20"
            />
        </div>

        <div class="btn_container">
            <a href="#"><btn text="SIGN UP" /></a>
            <a href="#"><btn theme="white" text="LOG IN" /></a>
        </div>
    </div>
</template>

<script>
import btn from '../assets/btn.vue';
export default {
    name: 'Header',
    components: { btn },
    data() {
        return {
            text: '!button template!!',
        };
    },
};
</script>

<style>
.header_container {
    background-color: rgb(0, 0, 0, 0.3);
    display: flex;
    height: 70px;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
}

.navicons img {
    margin: 0 15px;
}
</style>
