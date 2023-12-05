<template>
<p> Reaction time - {{ score }} ms</p>
<p class="rank"> {{ rank }}</p>
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
        if (this.score < 250) {
            this.rank = 'Speedstar'
        } else if (this.rank < 400) {
            this.rank = 'average gamer'
        } else {
            this.rank = 'could not be much worse'
        }
    }
    
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: green;
        font-weight: bold;
    
    }
</style>
