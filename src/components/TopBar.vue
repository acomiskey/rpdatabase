<script setup>
</script>

<template>
    <div id = "top-bar">
        <div id = "site-icon">
            icon here
        </div>
        <div id = "top-buttons">
            <button class = "nav-button">
                apply
            </button>
            <button class = "nav-button">
                reserve
            </button>
            <button class = "nav-button">
                about
            </button>
            <button class = "nav-button">
                log in
            </button>
        </div>
    </div>
</template>

<style scoped>
#top-bar
{
    width: 100%;
    height: 50px;
    background-color: black;
}

#site-icon
{
    float: left;
    height: 44px;
    width: 44px;
    margin-top: 3px;
    margin-left: 3px;
    background-color: blue;
    word-wrap: normal;
    text-align: center;
}

#top-buttons
{
    float: right;
    height: 100%;
    width: 90%;
    padding-right: 10px;
    padding-top:10px;
    text-align: right;
}

.nav-button
{
    width: 150px;
    height: 30px;
    font-size: 14pt;
    margin-left: 20px;
}
</style>