<script setup>
import { useSlots, ref , provide} from 'vue'
const slots = useSlots()
const tabTitles = ref(slots.default().map(tab => tab.props.title))
const selectedTitle = ref(tabTitles.value[0])
provide('selectedTitle', selectedTitle)
</script>

<template>
    <div class="tabs">

        <ul class="tabs__header">

            <li 
                v-for="title in tabTitles" 
                :key="title"
                class="tabs__item"
                :class="{ selected: selectedTitle === title}"
                @click="selectedTitle = title"
            >
                {{ title }}
            </li>

        </ul>

        <slot />
    </div>
</template>

<style>
.tabs 
{
    width: 100%;
}

.tabs__header 
{
    list-style: none;
    padding: 0;
    margin: 0;
    height: 40px;
    display: flex;
    text-align: left;
}

.tabs__item 
{
    font-size: 14pt;
    padding: 5px 100px;
    background-color: #eee;
    text-align: center;
    cursor: pointer;
    user-select: none;
}

.tabs__item.selected 
{
    background-color: #bfbfbf;
}

.tabs__content 
{
    background-color: #bfbfbf;
    min-height: 300px;
    display: grid;
    place-items: center;
    padding: 10px;
}
</style>