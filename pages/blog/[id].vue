<template>
    <div>
        <p class="blog">my blog with nice looking {{ id }}</p>
        <p>learn with joseph blog will aim you to learn more about tech that exit</p>
    </div>
</template>

<script setup>
const { id } = useRoute().params
</script>

<style   scoped>
 #p .blog{
    padding: auto;
    margin-bottom: 20pt;
    color: aqua;
    font-size: 50px;
 }
</style>