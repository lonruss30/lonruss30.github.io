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
    padding-top: 10px;
    padding-bottom: 10px;
    align-content: center;
    height: 5.5rem;
    width: 100%;
}

.name-logo {
    padding-left: 40px;
    font-family: 'Poppins', sans-serif;
    font-size: small;
}


@media only screen and (min-width: 1000px) {
    .navbar-main-container {
        font-family: 'Poppins', sans-serif;
        padding-top: 50px;
        padding-bottom: 20px;
        align-content: center;
        height: 5.5rem;
        width: 100%;
    }

    .name-logo {
        padding-left: 150px;
        font-size: larger;
    }

    .nav-buttons {
        padding-right: 150px;
    }

    .icon-class {
        margin-right: 10px;
    }

    .nav-buttons a {
        color: inherit;
        text-decoration: none;
        font-size: 24px;
        padding-right: 5px;
        cursor: pointer;
    }
}
</style>