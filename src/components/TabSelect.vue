<script setup>
import TabsWrapper from './TabsWrapper.vue'
import TabItem from './TabItem.vue'
</script>

<template>
    <TabsWrapper>
        <TabItem title="Characters">Characters will appear here</TabItem>
        <TabItem title="Reserves">Reserves will appear here</TabItem>
    </TabsWrapper>
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
    background-color: purple;
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

#selected
{
    background-color: purple;
}

#unselected
{
    background-color: orange;
}

#unselected:hover
{
    background-color: black;
    cursor: pointer;
}

.selector
{
    margin-left: 20px;
}
</style>