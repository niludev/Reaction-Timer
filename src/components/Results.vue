<template>
  <p>Reaction: {{score}} ms </p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return {
            rank: null
        }
    },
    /* when the component created in DOM: */
    mounted() {
        if(this.score < 300) {
            this.rank = "Grate job!"
        } else if(this.score < 600) {
            this.rank = "Not bad!"
        } else {
            this.rank = "That was too slow!"
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf78;
        font-weight: bold;
    }
</style>