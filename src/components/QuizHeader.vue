<script setup>
    import { defineProps } from 'vue';

    const {questionStatus, barPrecentage} = defineProps(["questionStatus", "barPrecentage"]);
</script>

<template>
    <header>
        <h4>Question {{ questionStatus }}</h4>
        <div class="bar">
            <div class="completion" :style="{width: barPrecentage}"></div>
        </div>
    </header>
</template>

<style scoped>
    header {
        margin-top: 20px;
    }

    header h4 {
        font-size: 30px;
    }

    .bar {
        width: 100%;
        height: 50px;
        border: 3px solid bisque;
    }

    .completion {
        height: 100%;
        width: 0%;
        background-color: bisque;
    }
</style>