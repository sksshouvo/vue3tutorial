<template>
    <div>{{greet}} {{name}}</div>    
    <div v-text="testText"></div>
    <div v-html="renderHtml"></div>
    <h2 v-bind:id="headingId">Test Heading</h2>
    <button type="button" v-bind:disabled="isDisabled">Disabled Button</button>
    <h2 class="underline">Underline Text</h2>
    <h2 class="underline" v-bind:class="status">Status</h2>
    <h1 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h1>
    <h2 v-bind:class="soldOut ? 'soldout' : 'new'">Sold-Out? Movie</h2>
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
            isDisabled: true,
            status: "danger",
            isPromoted: true,
            soldOut: false
        }
    }
}
</script>

<style scoped>
    .underline{
        text-decoration: underline;
    }
    .promoted {
        font-style: italic;
    }
    .soldout {
        color: red;
    }
    .new {
        color: green;
    }
</style>