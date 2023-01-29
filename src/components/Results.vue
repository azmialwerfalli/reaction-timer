<template>
  <h1>The result is : {{ res }}</h1>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return {
            res: null
        }
    },
    mounted() {
        this.res = this.score
    },
    methods:{

    }
}
</script>

<style>

</style>