<template>
  <div class="w-60 bg-green-500 block" v-if="showBlock" @click="stopTimer">
    click me
  </div>
</template>

<script>

export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false,
            timer: null,
            reactionTime: 0,
        }
    },
    methods: {
        startTimer() {
            this.timer = setInterval(() => {
                this.reactionTime += 10;
            }, 10);
        },
        stopTimer() {
            clearInterval(this.timer);
            console.log(this.reactionTime);
            this.$emit('end', this.reactionTime)
        }
    },
    mounted() {
        console.log('componet monuted');
        setTimeout(() => {
            this.showBlock = true;
            this.startTimer();
            console.log(this.delay);
        }, this.delay)
    },
    updated() {
        console.log('updated');
    }

}
</script>


<style scoped>
    .block{
        padding: 100px 0;
        border-radius: 20px;
        text-align: center;
        margin: 40px auto;
    }
</style>