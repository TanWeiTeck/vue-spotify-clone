<template>
    <div class="menu_container">
        <img
            class="spotify_logo"
            src="https://storage.googleapis.com/pr-newsroom-wp/1/2018/11/Spotify_Logo_RGB_White.png"
            alt="spotify_logo"
            width="130"
        />
        <div>
            <img
                src="https://img.icons8.com/fluency-systems-filled/48/ffffff/home.png"
                width="25"
            />
            <a href="">Home</a>
        </div>
        <div>
            <img
                src="https://img.icons8.com/ios-glyphs/30/ffffff/search--v1.png"
                width="25"
            />
            <a href="">Search</a>
        </div>
        <div>
            <img
                src="https://img.icons8.com/ios-glyphs/30/ffffff/menu--v1.png"
                width="25"
            />
            <a href="">Your Library</a>
        </div>
        <br />
        <div>
            <img
                src="https://img.icons8.com/ios-filled/50/ffffff/plus-2-math.png"
                width="25"
            />
            <a href="">Create Playlist</a>
        </div>
        <div v-for="playlist in playlists" :key="playlist.id">
            <img :src="playlist.logo" width="25" alt="" />
            <a href="">{{ playlist.label }}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Menu',
    data() {
        return {
            playlists: [
                {
                    id: 1,
                    logo: 'https://i.pinimg.com/originals/fe/5c/36/fe5c36b8b4cbaa728f3c03a311e002cb.png',
                    label: 'Liked Songs',
                },

                {
                    id: 2,
                    logo: 'https://i.pinimg.com/originals/fe/5c/36/fe5c36b8b4cbaa728f3c03a311e002cb.png',
                    label: 'English Song',
                },
                {
                    id: 3,
                    logo: 'https://i.pinimg.com/originals/fe/5c/36/fe5c36b8b4cbaa728f3c03a311e002cb.png',
                    label: 'WT Playlist',
                },
            ],
        };
    },
};
</script>

<style scoped>
.menu_container {
    display: flex;
    flex-direction: column;
    background: black;
    height: 100vh;
}

.menu_container div {
    padding: 10px 20px;
    cursor: pointer;
    display: flex;
    align-items: center;
    background-image: linear-gradient(black, black); /*bg image*/
    opacity: 0.7;
    transition-duration: 0.5s;
}
.menu_container div:hover {
    opacity: 1;
}

.spotify_logo {
    margin: 20px;
}
.menu_container a {
    text-decoration: none;
    color: white;
    font-size: 13px;
    font-weight: 400;
    margin-left: 20px;
}
</style>
