<template>
    <div class="card">
        <div class="image">
            <img class="profile-image" src="./../assets/profile-img.png" alt="John" style="width:40%">
        </div>
        <div class="text">
            <h1>My Profile</h1><br/>
            <p class="name">{{username}}</p><button type="button" class="username_button" onclick="">Edit</button><br/><br/>
            <p class="number">Phone number: {{phoneNumber}}</p><button type="button" class="username_button" onclick="">Edit</button><br/><br/>
            <p class="email">Email address: {{emailaddress}}</p><button type="button" class="username_button" onclick="">Edit</button><br/><br/>
            <div>
                <h3>SMS ALERT ACTIVATION</h3>
                <input type="checkbox" class="myCheck" onclick="activateSMS()"><br/><br/>
            </div>

        </div>
        <p><button class="save">Save</button></p>

    </div>
</template>

<script>
    export default {
        name: "Profile",
        methods:{
            activateSMS: function(){
                if (!this.isActivated){
                    this.isActivated='true'
                }
                else if(this.isActivated){
                    this.isActivated=false
                }
            }
        },
        data () {
            return {
                username: 'John Doe',
                phoneNumber: '+48 789-263-109',
                emailaddress: 'john.doe1@mail.com',
                isActivated: false
            }
        }
    }
</script>

<style scoped>
    h1{
        box-shadow: inset 0 0px 0 white, inset 0 -1px 0 rgba(40,40,40,0.29);
    ;

    }
    h3, .name, .number, .email{
        display: inline;
        margin-right: 10px;
    }
    .profile-image{
        border-radius: 50%;
    }
    .card {
        background: rgba(255,255,255,0.74);
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        max-width: 600px;
        margin: auto;

    }

    .title {
        color: grey;
        font-size: 18px;
    }

    .save {
        border: none;
        outline: 0;
        display: inline-block;
        padding: 8px;
        color: white;
        background-color: rgba(40,40,40,0.89);
        text-align: center;
        cursor: pointer;
        width: 100%;
        font-size: 18px;
    }
    .username_button{
        border: none;
        outline: 0;
        display: inline-block;
        padding: 1px;
        color: white;
        background-color: rgba(40,40,40,0.89);
        text-align: center;
        cursor: pointer;
        width: 10%;
        font-size: 13px;
        float: right;

    }

    a {
        text-decoration: none;
        font-size: 22px;
        color: black;
    }

    button:hover, a:hover {
        opacity: 0.7;
    }
    .image{
        text-align: center;
        margin-top:20px;
    }
    .text{
        font-family: Dosis, sans-serif;
        margin: 20px 30px;

    }
    .myCheck{
        background-color: #2c3e50;

    }
</style>
