<template>
    <div class="navbar-main-container">
        <div class="name-logo">
            <h2>lonrussel</h2>
        </div>
        <div class="nav-buttons-container">
            <div v-for="(items, index) in informationData.InfoArray" v-bind:key="items" class="nav-buttons">
                <a :href="[informationData.InfoArray[index].GithubLink]" target="_blank" rel="noopener noreferrer"><i
                        class="fa-brands fa-github icon-class"></i></a>
                <a :href="[informationData.InfoArray[index].LinkedInLink]" target="_blank" rel="noopener noreferrer"><i
                        class="fa-brands fa-linkedin icon-class"></i></a>
            </div>
        </div>
    </div>

</template>
<script>
import infoData from "../data/info.json"
export default {
    data() {
        return {
            informationData: infoData
        }
    }
}
</script>
<style scoped>
.navbar-main-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-content: center;
    height: 5.5rem;
    width: 100%;
}

.name-logo {
    font-family: 'Poppins', sans-serif;
}

.nav-buttons a {
    color: inherit;
    text-decoration: none;
    cursor: pointer;
}

@media screen and (min-width: 334px) {
    .navbar-main-container {
        padding: 10px 40px 10px 40px;
    }

    .name-logo {
        font-size: 18px;
    }

    .nav-buttons{
        font-size: 24px;
    }

    .nav-buttons a{
        padding-left: 10px;
    }
}

@media screen and (min-width: 720px) {
    .navbar-main-container {
        padding: 10px 80px 10px 80px;
    }

    .name-logo {
        font-size: 18px;
    }

    .nav-buttons{
        font-size: 26px;
    }

    .nav-buttons a{
        padding-left: 15px;
    }
}

@media screen and (min-width: 1095px) {
    .navbar-main-container {
        padding: 10px 150px 10px 150px;
    }

    .name-logo {
        font-size: 18px;
    }

    .nav-buttons{
        font-size: 26px;
    }

    .nav-buttons a{
        padding-left: 15px;
    }
}
</style>