<template>
  <div class="index">
  <div>카운트 : {{count}}</div>
  <button v-on:click="bClick">클릭해보세요.</button>
  </div>
  <button @click="play('http://172.30.1.1/deagum.mp4')">audioPlayer</button>
</template>

<script>
export default {
    methods:{
        play(file){
            if(file){
                var audio = new Audio(file);
                audio.play();
            }
        },
        bClick(){
            // alert('!')
            this.count += 1
        }
    },
    data(){
        return{
            count:1
        }
    }
}
</script>

<style>

</style>