<template>

    <div class="posts">

        <img src="../assets/img/facebook.svg" alt="facebook" class="logo">
        <CardComp 
        class="mt-2 mx-auto single-post"        
        picture="https://images.pexels.com/photos/11035366/pexels-photo-11035366.jpeg?auto=compress&cs=tinysrgb&w=600"
        parrafo="primera carta" :header="{ name: 'Wilmar rojas', picture:'https://randomuser.me/api/portraits/men/3.jpg'}"
        :likes="true"/>        
        <CardComp 
        class="mt-2 mx-auto single-post"
        picture="https://images.pexels.com/photos/7504859/pexels-photo-7504859.jpeg?auto=compress&cs=tinysrgb&w=600"
        parrafo="segunda carta" :header="{ name: 'Salomon rojas', picture:'https://randomuser.me/api/portraits/men/3.jpg'}"
        :likes="true"/>    
        <CardComp 
        class="mt-2 mx-auto single-post"
        picture="https://images.pexels.com/photos/6424583/pexels-photo-6424583.jpeg?auto=compress&cs=tinysrgb&w=600"
        parrafo="tercera carta" :header="{ name: 'Guiomar rojas', picture:'https://randomuser.me/api/portraits/men/3.jpg'}"
        :likes="true"/>        
        
    </div>    

</template>

<script>

    import CardComp from '../components/CardComp.vue';

    export default{
        name: "PostsView",
        components: {
            CardComp
        }
    }

</script>

<style>
    .posts{
        min-height: 60vh;
        max-width: 895px;
        margin: auto;
    }
    .logo{
        max-width: 115px;
        padding: 0.2 rem;
    }
    .single-post{
        max-width: 550px;
    }
</style>