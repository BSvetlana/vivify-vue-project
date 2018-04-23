<template>
    <div>
       <table>
           <thead>
                <th>First Name</th>
                <th>Last Name</th>
                <th>Email</th>
           </thead>
           <tbody  v-for="(contact,key) in contacts" :key="key" >
           <tr>
               <td>
                   {{contact.firstName}}
               </td>
               <td>
                   {{contact.lastName}}
               </td>
               <td>
                   {{contact.email}}
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
                ]

            }
        }
    }
</script>

<style scoped>

</style>