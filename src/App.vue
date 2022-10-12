<template>
    <active-user
    :name="contacts.name"
    :age="contacts.age"
    >
    </active-user>
    <user-data
    @add-person="addNewContact">
    </user-data>
</template>


<script>
export default {
    data(){
        return{
           contacts:{
                    id: "",
                    name: "User Name: ",
                    age: "User Age: "
                },
            }
    },
    methods: {
        addNewContact(name, age){
            this.contacts = {
                id: new Date().toISOString(),
                name: name,
                age: age
            };
        }
    }

}
</script>

<style>

    html {
        font-family: sans-serif;
    }

    section {
        margin: 2rem auto;
        max-width: 40rem;
        border-radius: 12px;
        border: 1px solid #ccc;
        padding: 1rem;
    }
</style>
