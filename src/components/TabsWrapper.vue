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
    display: flex;
    text-align: left;
    gap: 5px;
}

.tabs__item 
{
    flex: 1;
    background-color: #eee;
    padding: 5px 0;
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