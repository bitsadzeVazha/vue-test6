<template>
    <section>
        <label>Name</label>
        <input type="text" v-model="enteredName">
        <label> Age</label>
        <input type="text"  v-model="enteredAge">
        <button @click="addPerson">Add</button>
    </section>
</template>

<script>
export default {
    emits: ['add-person'],
    data(){
        return{
            enteredName: "",
            enteredAge: ""
        }
    },
    methods: {
        addPerson(){
            this.$emit("add-person", this.enteredName, this.enteredAge);
        }
    }
}
</script>
