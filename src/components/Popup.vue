<template>
    <div>
        <div class="box">
            <a class="button" href="#popup1">Edit</a>
        </div>
    <div id="popup1" class="overlay">
        <div class="popup">
            <h2>Here i am</h2>
            <a class="close" href="#">&times;</a>
            <div class="content">
                Thank to pop me out of that button, but now i'm done so you can close this window.
            </div>
        </div>
    </div>
    </div>
</template>

<script>
    export default {
        name: "Popup"
    }
</script>

<style scoped>


    h1 {
        text-align: center;
        font-family: Tahoma, Arial, sans-serif;
        color: grey;
        margin: 80px 0;
    }

    .box {
        width: 40px;
        height: 40px;

        margin: 0 auto;
        padding: 25px;
        background-clip: padding-box;
        text-align: center;
        float: right;
    }

    .button {
        border: none;
        outline: 0;
        display: inline-block;
        padding: 5px;
        color: white;
        background-color: rgba(40,40,40,0.89);
        text-align: center;
        cursor: pointer;
        font-size: 13px;
        float: right;
        position: absolute;

    }
    .button:hover {
        color: grey;
    }

    .overlay {
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        background: rgba(0, 0, 0, 0.7);
        transition: opacity 500ms;
        visibility: hidden;
        opacity: 0;
    }
    .overlay:target {
        visibility: visible;
        opacity: 1;
    }

    .popup {
        margin: 70px auto;
        padding: 20px;
        background: #fff;
        border-radius: 5px;
        width: 30%;
        position: relative;
        transition: all 5s ease-in-out;
    }

    .popup h2 {
        margin-top: 0;
        color: #333;
        font-family: Tahoma, Arial, sans-serif;
    }
    .popup .close {
        position: absolute;
        top: 20px;
        right: 30px;
        transition: all 200ms;
        font-size: 30px;
        font-weight: bold;
        text-decoration: none;
        color: #333;
    }
    .popup .close:hover {
        color: grey;
    }
    .popup .content {
        max-height: 30%;
        overflow: auto;
    }

    @media screen and (max-width: 700px){
        .box{
            width: 40%;
        }
        .popup{
            width: 70%;
        }
    }
</style>
