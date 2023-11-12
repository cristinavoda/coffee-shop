<template>
    <nav>
        <img id="logo-nav" alt="logo" src="../../public/img/Starbucks-logo.png"/>
        <ul class="nav-items">
            <li> Item 1 </li>
            <li> Item 2 </li>
            <li> Item 3 </li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: "Navbar",
    data(){
        return {

        }
    }
}
</script>

<style>
nav {
    display: flex;
    justify-content: space-between;
    padding-right: 5%;
    padding-left: 5%;
    padding-top: 1%;
    padding-bottom: 1%;
    background-color: rgba(244, 129, 79, 0.605);
}

.nav-items {
    display: flex;
    justify-content: space-around;
    color: rgb(25, 25, 25);
    list-style: none;
    gap: 2rem;
    align-items: center;

}

#logo-nav {
    width: 50px;
}
</style>