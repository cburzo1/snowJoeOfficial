<template>
<div class = "Panel">
    <div class = "panelContent">
        <p>{{question.question}}</p>
        <!--<input type="radio" :name = "question.choices">
        <label >{{question.choices[0]}}</label><br>
        <input type="radio" :name = "question.choices">
        <label >{{question.choices[1]}}</label><br>
        <input type="radio"  :name = "question.choices">
        <label >{{question.choices[2]}}</label><br>
        <input type="radio"  :name = "question.choices">
        <label >{{question.choices[3]}}</label><br>
        <input type="radio"  :name = "question.choices">
        <label >{{question.choices[4]}}</label><br>-->
        <Question :choices = "question.choices"/>
    </div>
</div>
</template>

<script>
import Question from './Question.vue';

export default{
    name: 'Panel',
    props: {
        question: Object
    },
    components: {
        Question
    }
}
</script>

<style scope>
.Panel{
    border: 1px solid white;
    height: 215px;
    border-radius: 5px;
    box-shadow:0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    margin: 12px;
    background-color: white;
}

.panelContent{
    margin-left: 25px;
}
</style>
