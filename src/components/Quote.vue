<template>
    <div class="well quote">
        <slot></slot>
    </div>
</template>

<script>
    export default {
    }
</script>

<style>
    .quote {
        background-color: white;
        font-family: Arizonia, monospace;
        font-size: xx-large;
        cursor: pointer;
    }

    .quote:hover {
        background-color: palevioletred;
    }

</style>
