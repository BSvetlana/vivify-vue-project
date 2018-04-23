<template>
    <div>
        <form @submit.prevent ="addContact">

            <label>First Name</label>
            <input type="text" placeholder="First Name" v-model="newContact.firstName"/>

            <label>Last Name</label>
            <input type="text" placeholder="Last Name" v-model="newContact.lastName"/>

            <label>Email</label>
            <input type="email" placeholder="Your Email" v-model="newContact.email"/>

            <button type="submit">Add Contact</button>
        </form>
       <table>
           <thead>
                <th>First Name</th>
                <th>Last Name</th>
                <th>Email</th>
                <th>&nbsp;</th>
           </thead>
           <tbody>
           <tr v-for="(contact,key) in contacts" :key="key">
               <td>
                   {{contact.firstName}}
               </td>
               <td>
                   {{contact.lastName}}
               </td>
               <td>
                   {{contact.email}}
               </td>
               <td>
                   <button @click="removeContact(contact)">Remove</button>
               </td>
           </tr>
           </tbody>

       </table>
    </div>
</template>

<script>

    export default {
        name: "ContanctsList",
        data(){

            return {
                contacts: [
                    {firstName: 'John', lastName: 'Jonson', email: 'john@jonhson.com'},
                    {firstName: 'Don', lastName: 'Donson', email: 'don@donson.com'},
                    {firstName: 'Stiv', lastName: 'Stivenson', email: 'stiv@stivenson.com'}
                ],

                newContact: {
                    firstName: '',
                    lastName: '',
                    email: ''
                }
            }
        },
        methods: {
            addContact(){
                this.contacts.push(this.newContact);
                this.newContact = {}
            },
            removeContact(contact){
                this.contacts.splice(this.contacts.indexOf(contact));
            }
        }
    }
</script>

<style scoped>

</style>