<script setup>
</script>

<template>
    <div id = "tabs-bar">
        <div class = "tab">
            characters
        </div>
        <div class = "tab">
            reserves
        </div>
    </div>
    <div id = "control-bar">
        <select class = "selector">
            <option value="all">Writer</option>
            <option value="test-name">Example Writer Name</option>
        </select>
        <select class = "selector">
            <option value = "all">Fandom</option>
            <option value = "test-fandom">Example Fandom</option>
        </select>
        <select class = "selector">
            <option value = "default">Sort</option>
            <option value = "oldest-first">Oldest to Newest</option>
            <option value = "newest-first">Newest to Oldest</option>
            <option value = "alpha-char">Alpha by Character</option>
            <option value = "alpha-fandom">Alpha by Fandom</option>
            <option value = "alpha-writer">Alpha by Writer</option> 
        </select>
    </div>
    <div id = "results-box">
        this is where the search results will go
    </div>
</template>

<style scoped>
#tabs-bar
{
    width: 100%;
    height: 50px;
    background-color: yellow;
    text-align: left;
}

#control-bar
{
    width: 100%;
    height: 30px;
    background-color: purple;
    text-align: right;
    padding-right: 20px;
}

#results-box
{
    width: 100%;
    background-color: navy;
    padding: 50px;
}

.tab
{
    display: inline-block;
    height: 100%;
    width: 200px;
    background-color: orange;
    text-align: center;
    font-size: 14pt;
    padding-top: 10px;
}

.selector
{
    margin-left: 20px;
}
</style>