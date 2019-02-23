<template lang="html">
    <section class="message">
        <h1>message Component</h1>
        <h1>{{messageData}}</h1>
        <appInput :msg="messageData" @ordreModifierParent="modifierParent($event)"
                  @messageChanged="messageData= $event"></appInput>
        <br>prop1{{prop1}}
        <br>
        <button @click="init">init</button>
        <button @click="modifier"> modifier</button>

    </section>
</template>

<script lang="js">
    import appInput from "./input.vue";

    export default {
        name: 'message',
        props: ['prop1'],
        data() {
            return {
                messageData: 'un message de composant message ! '
            }
        },
        components: {
            appInput
        },
        methods: {

            modifierParent: function (event) {
                console.log("this.prop1" + this.prop1)
                this.prop1 = event;
                console.log("this.prop1" + this.prop1)
            }, modifier: function () {

                this.prop1 = "updated"
            },
            init: function () {
                this.prop1 = "original"


            },

        }
    }
</script>

<style scoped lang="scss">
    .message {

    }
</style>
