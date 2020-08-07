<template>
    <div>
        <img class="profile-image" src="./../assets/profile-img.png" alt="John" style="width:10%">

    <div class="dropdown">
        <button class="dropbtn">Dropdown</button>
        <div class="dropdown-content">
            <a href="#">Logout</a>
            <a href="#">Profile</a>
            <a href="#">Settings</a>
        </div>
    </div>
    </div>
</template>

<script>
    export default {
        name: "Login"

    }
</script>

<style scoped>
    .profile-image{
        float: end;
    }
    /* Dropdown Button */
    .dropbtn {
        background-color: rgba(0, 165, 195,0.15);
        padding: 16px;
        font-size: 16px;
        border: none;
    }

    /* The container <div> - needed to position the dropdown content */
    .dropdown {
        position: relative;
        display: inline-block;
        float: right;
    }

    /* Dropdown Content (Hidden by Default) */
    .dropdown-content {
        display: none;
        position: absolute;
        right: 0;

        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        z-index: 1;
    }

    /* Links inside the dropdown */
    .dropdown-content a {
        padding: 12px 16px;
        text-decoration: none;
        display: block;
    }

    /* Change color of dropdown links on hover */
    .dropdown-content a:hover {        background-color: rgba(0, 165, 195,0.15);
    }

    /* Show the dropdown menu on hover */
    .dropdown:hover .dropdown-content {display: block;}

    /* Change the background color of the dropdown button when the dropdown content is shown */
    .dropdown:hover .dropbtn {        background-color: rgba(0, 165, 195,0.35);
    }
</style>
