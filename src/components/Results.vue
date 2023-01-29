<template>
  <h1>The result is : {{ res }} </h1>
  <p class="rank" :class="rankStyle">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return {
            rank: null,
            res: null,
            rankStyle: null,
        }
    },
    mounted() {
        this.res = this.score
        if(this.res <= 250){
            this.rank = "Ninja Fingers"
            this.rankStyle = 'fast'
        }else if (this.res < 400 ){
            this.rank = "Reflexer"
            this.rankStyle = 'normal'
        }else {
            this.rank = "Snail Sludge ..."
            this.rankStyle = 'slow'
        }
        console.log(this.rank)
    },
    

}
</script>

<style>
    .rank {
        font-size: 1.4rem;
        font-weight: bold;
    }
    .fast {
        color: #0faf87; 
    }
    .normal {
        color: #0b35b3;
        
    }
    .slow {
        color: rgb(175, 15, 15);

    }
</style>