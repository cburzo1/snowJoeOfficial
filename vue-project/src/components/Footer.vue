<template>
<div class = "Footer">
    <button @click="onClick" class = "Button">Submit</button>
    <p></p>
</div>
</template>

<script>
export default{
    name: 'Footer',
    methods: {
        onClick(e){
            e.preventDefault();

            console.log("CLICKED");
        }
    }
}
</script>

<style scope>
    .Footer{
        margin: auto;
        width: 10%;
    }
    .Button{
        background-color: green;
        color: white;
        border: 2px solid black;
        border-radius: 3px 3px;
        height: 35px;
        width: 75px;
    }
</style>
