<template>

    <div class="card-header"> 
        <div class="row">
            <div class="col-2 col-sm-2">
                <img class="avatar-img" :src="header.picture" alt="Avatar Wilmar">
            </div>
            <div class="col-8 col-sm-8">
                <h4 class="card-header-title m-0">
                    <router-link to="/profile">
                        {{header.name}}
                    </router-link>
                </h4>
                <small class="text-muted card-header-subtitle">Hace dos minutos</small>
            </div>
            <div class="col-1">
                <button class="btn d-flex align-items-center more-btn">
                    <span class="material-icons-outlined">
                    more_horiz</span>
                </button>
            </div>
        </div>           
    </div>   
    
</template>

<script>

    export default{
        name: "CardHeader",
        props: ["header"]
    }

</script>

<style scoped>

.card-header{
    background-color: transparent;
    padding: 0.5rem 1rem;
    padding-bottom: 0;
    border-bottom: none;
}
.avatar-img{
    width: 40px;
    height: 40px;
    object-fit: cover;
    border-radius: 50%;
}
.card-header-title{
    line-height: 0.7;
}
.card-header-subtitle{
    font-size: 0.8em;
}
@media (min-width: 576px){
    .card-header .col-8{
        margin-left: -1.9em;
    }
}

</style>