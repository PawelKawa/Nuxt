<template>
    <div>
        <p class="text-center">reaction time - {{ scorE }} ms</p>
        <p class="text-center">{{ rank }}</p>
    </div>
</template>

<script>
export default {
    props: ['scorE',],
    data() {
        return {
            rank :null
        }
    },
    methods: {},
    mounted() {
        if (this.scorE < 250) {
            this.rank = 'ninja fingers'
        } else if (this.scorE < 400) {
            this.rank = 'rapid one'
        } else if (this.scorE < 800) {
            this.rank = 'could be faster'
        } else {
            this.rank = 'lol granny'
        }
    }
}
</script>

<style>

</style>