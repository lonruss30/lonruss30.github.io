<template>
    <div class="navbar-main-container">
        <div class="name-logo"> <h2>Lon Russel</h2></div>
        <div class="nav-buttons-container">
            <div class="nav-buttons">
                <a href="">Projects</a>
                <a href="">Experiences</a>
                <a href="">Contacts</a>
                <a href="">Resume</a>
            </div>
        </div>
    </div>
        
</template>
<script>
export default {
    
}
</script>
<style>
    .navbar-main-container{
        display: flex;
        flex-wrap: wrap;
        padding-top: 10px;
        padding-bottom: 10px;
        justify-content: space-between;
        height: 3rem;
        width: 100%;
        position: fixed;
        background-color: #F0EBCE;
    }
    .name-logo{
        float: left;
        height: inherit;
        width: 300px;
    }
    .name-logo h2{
        margin: 0;
        margin-top: 8px;
    }

    .nav-buttons-container{
        display: inline-block;
        width: 300px;
        margin-right: 50px;
    }

    .nav-buttons-container a{
        font-size: .837rem;
        font-weight: 500;
        text-decoration: none;
        color: #395144;
        margin: 5px;
    }

    .nav-buttons-container a:hover{
        color: #AA8B56;
    }

    .nav-buttons{
        padding-top: 10px;
    }
    
</style>