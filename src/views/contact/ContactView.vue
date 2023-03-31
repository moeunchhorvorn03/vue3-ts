<template>
    <div >
        <h1>Contact</h1>
            <div :key="contact.id" v-for="contact in contacts">
                <router-link class="link" :to="{ name: 'contactDetails' , params: { id: contact.id } }">
                    <p>Email: {{ contact.email }}</p>
                    <p>Phone: {{ contact.email }}</p>
                    <p>Address: {{ contact.email }}</p>
                    <hr size="1">
                </router-link>
            </div>
    </div>
</template>

<script>

export default{
   data(){
    return{
        contacts: []
    }
   },
   mounted(){
        fetch('http://localhost:3000/contact')
            .then(res => res.json())
            .then(data => this.contacts = data)
            .catch(err => console.log(err.message))
   }
}
</script>

<style scoped>
p {
    background-color:rgb(200, 200, 200);
    padding: 10px;
    color: #2c3e50;
}
.link{
    text-decoration: none;
}

</style>