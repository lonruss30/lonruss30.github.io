<template>
    <div class="navbar-main-container">
        <div class="name-logo">
            <h2>lonrussel</h2>
        </div>
        <div class="nav-buttons-container">
            <div class="nav-buttons">
            </div>
        </div>
    </div>

</template>
<script>
export default {

}
</script>
<style scoped>
.navbar-main-container {
    display: flex;
    flex-wrap: wrap;
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
        padding-top: 50px;
        padding-bottom: 20px;
        align-content: center;
        height: 5.5rem;
        width: 100%;
    }

    .name-logo {
        padding-left: 80px;
        font-size: larger;
    }
}
</style>