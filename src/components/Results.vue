<template>
    <div class="results">
        <p>your score: {{score}}ms. </p>
        <p class="rank"> {{ rank }}</p>
    </div>
</template>

<script>
export default {
    props: ['score'],
data() {
    return {
        rank: null
    }
    },
mounted() {
    if (this.score < 200) {
        this.rank = 'Amazing'
    } else if (this.score < 400) {
        this.rank = 'Rapid Reflexes'
    } else if (this.score < 600) {
        this.rank = 'Good'
    } else {
        this.rank = 'Snail pace, but you can do better.'
    }
},
}
</script>

<style>
.rank {
    font-size: 1.4rem;
    font-weight: bold;
    color: #0faf87;
}
</style>