<template>
    <div class="test">
        <input type="text" v-model="title"><br>
        <h1>{{title}}</h1>
        <p v-if="showName">{{user.firstName}}</p>
        <p v-else>Nobody</p>
        <ul>
        </ul>
        <button v-on:click="greet">Say greeting</button><br>
        <input type="text" v-on:keyup="pressKey">
        <h2>{{msg}}</h2>
    </div>
</template>

<script>
export default {
    name: 'Test',
    props: {
        msg: {
            type: String,
            default: 'Foobar'
        }
    },
    data(){
        return {
            title: 'Hello World',
            user: {
                firstName: 'John',
                lastName: 'Doe'
            },
            showName: true,
            items: [
                {title:'item one'},
                {title:'item two'},
                {title:'item three'}
            ]
        }
    },
    methods: {
        greet: function(){
            alert('Hello!');
        },
        pressKey: function(e){
            console.log("e.target.value")
        }
    }
}
</script>

<style scoped>

</style>

