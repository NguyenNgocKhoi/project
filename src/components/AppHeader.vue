<template>
    <nav class="navbar navbar-expand navbar-dark bg-primary">
        <a href="/" class="navbar-brand">
            <img class="navbar navbar-logo" src="../assets/logo.png">
        </a>
    
        <div class="mr-auto navbar-nav ">
            <li class="nav-item  ">
                <router-link :to="{ name: 'ContactBook' }" class="nav-link">
                   All note
                    <!-- <i class="fas fa-address-book"></i> -->
                </router-link>
            </li>
            <li class="nav-item">
                <router-link :to="{ name: 'ContactBook' }" class="nav-link">
                  Flagged
                    <!-- <i class="fas fa-address-book"></i> -->
                </router-link>
            </li>
        </div>
    </nav>
</template>
<style>
.navbar .navbar-logo{
    width:150px;
    height:60px;
    padding: 0;
}
.navbar-nav{
    margin-left:35%;
    font-size: 1.6rem;
}

.navbar-nav .nav-item:hover{
    border-radius:5px ;
    background-color:black;
    
}
</style>