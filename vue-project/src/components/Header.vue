<template>
    <div class = Header>
        <h6 class = "textAlign">Quiz Application</h6>
    </div>
</template>

<script>
export default{
    name: 'Header'
}
</script>

<style scope>
.Header{
    background-color: brown;
    color: white;
    height: 25px;
    display: flex;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
}
.textAlign{
    margin: 0px;
    padding: 0px;
    margin-left: 15px;
    line-height: 23px;
}
</style>
