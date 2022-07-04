<template>
<div v-for="question in questions">
    <Panel :question="question" :questionsArray="questions"/>
</div>
</template>

<script>
import Panel from './Panel.vue'

export default{
    name: 'Panels',
    props: {
        questions: Array
    },
    components: {
        Panel
    }
}
</script>

<style scope>
</style>
