<template>
<div class = "question" v-for="choice in choices">
    <input type="radio" :id = "choice" @change="onChange($event)" v-model="mChoice" :name = "choices" :value = "choice">
    <label :for = "choice">{{choice}}</label><br>
</div>
<p>{{mChoice}}</p>
</template>

<script>
import { VueElement } from 'vue';

export default{
    name: 'Question',
    data(){
        return{
            mChoice: null,
            arr: [0,0,0,0,0]
        }
    },
    methods: {
        onChange(e){
            var data = e.target.value;

            let val = {
                idx: 0,
                correctAns: ""
            };

            let arr2 = [...this.arr];

            this.questionsArray.forEach((i, index) => {
                if(e.target.name == i.choices){
                    val.idx = index;
                    val.correctAns = i.correctAnswer;
                    arr2.splice(index, 1, val);
                    this.arr = [...arr2];
                }
            });
            console.log( this.arr);
        }
    },  
    props: {
        choices: Array,
        questionsArray: Array
    }
}
</script>

<style scope>
    .question{
        margin: 12px;
    }
</style>
