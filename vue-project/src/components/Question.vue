<template>
<div class = "question" v-for="choice in choices">
    <input type="radio" :id = "choice" v-model="mChoice" :name = "choices" :value = "choice">
    <label :for = "choice">{{choice}}</label><br>
</div>
<p>{{mChoice}}</p>
</template>

<script>
export default{
    name: 'Question',
    data(){
        return{
            mChoice: null
        }
    },
    props: {
        choices: Array
    }
}
</script>

<style scope>
    .question{
        margin: 12px;
    }
</style>
