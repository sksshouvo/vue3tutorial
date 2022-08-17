<template>
    <div>{{greet}} {{name}}</div>    
    <div v-text="testText"></div>
    <div v-html="renderHtml"></div>
    <h2 v-bind:id="headingId">Test Heading</h2>
    <button type="button" v-bind:disabled="isDisabled">Disabled Button</button>
</template>
<script>
export default {
    name: "App",
    data () {
        return {
            greet: "Hello",
            name: "Salman Kabir",
            testText: "<b>Hi There</b>",
            renderHtml: `<a href='#' onClick="alert('Hello There')">Click me to get Alert</a>`,
            headingId: "heading",
            isDisabled: true
        }
    }
}
</script>

<style scoped>

</style>