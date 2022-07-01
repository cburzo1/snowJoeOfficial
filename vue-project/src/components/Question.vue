<template>
<div class = "question" v-for="choice in choices">
    <input type="radio" :id = "choice" :name = "choices" :value = "choice">
    <label :for = "choice">{{choice}}</label><br>
</div>
</template>

<script>
export default{
    name: 'Question',
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
