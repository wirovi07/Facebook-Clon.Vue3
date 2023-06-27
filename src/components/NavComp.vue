<template>

    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container justify-content-evenly">
            <RouterLink to="/" class="nav-link" 
            :class="{ active: activePath.home }"
            aria-current="page">
                <span class="material-icons-round">
                    home
                </span>
            </RouterLink>

            <RouterLink to="/about" class="nav-link"
            :class="{ active: activePath.about }"
            aria-current="page">
                <span class="material-icons-round">
                    info
                </span>
            </RouterLink>                   
                    
            <RouterLink to="/posts" class="nav-link" 
            :class="{ active: activePath.posts }"
            aria-current="page">
                <span class="material-icons-round">
                    featured_play_list
                </span>
            </RouterLink>                   
        </div>
    </nav>
    
</template>

<script>

    export default{
        name: 'NavComp',
        computed: {
            activePath(){
                if(this.$route.path === "/"){
                    return {
                        home: true,
                        about: false,
                        posts: false
                    }
                } else if(this.$route.path === "/about"){
                    return {
                        home: false,
                        about: true,
                        posts: false
                    }
                }else if(this.$route.path === "/posts"){
                    return {
                        home: false,
                        about: false,
                        posts: true
                    }
                }  else{
                    return {
                        home: false,
                        about: false,
                        posts: false,
                    }
                }  
            },
        },
    }

</script>

<style scoped>
    .material-icons-round{
        color: white;
        font-size: 1.4em;
        background-color: rgba(218, 218, 218, 0.158);
        padding: 0.3em;
        border-radius: 50%;
        margin: 0.1em;
    }
    .navbar{
        margin: 0;
        padding-bottom: 0;
        padding-top: 0;
    }    
    .nav-link{
        padding: 0.2rem 1rem;
    }
    .active .material-icons-round{
        color: white;
        background-color: rgba(133, 128, 128, 0.158);
        border: 1px solid rgba(248, 244, 244, 0.342);
    }

</style>