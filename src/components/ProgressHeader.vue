<template>
    <div>
        <h2>Quotes Added 2</h2>
        <div class="progress">
            <div class="progress-bar" role="progressbar" :aria-valuenow="numberOfQuotes" aria-valuemin="0" aria-valuemax="100"
                 style="min-width: 3em;"
                 :style="{width: numberOfQuotes*10 + '%'}">
                {{ numberOfQuotes }} / 10

            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['numberOfQuotes'],
    }
</script>

<style>

</style>
