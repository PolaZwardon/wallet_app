<template>
    <div class="card">
        <div class="image">
            <img class="profile-image" src="./../assets/profile-img.png" alt="John" style="width:40%">
        </div>
        <div class="text">
            <h1>My Profile</h1><br/>
            <p class="name">{{username}}</p><Popup :title=title :msg=msg id="pop1"></Popup><br/><br/>
            <p class="number">Phone number: {{phoneNumber}}</p><Popup :title=title :msg=msg id="pop2"></Popup><br/><br/>
            <p class="email">Email address: {{emailaddress}}</p><Popup :title=title :msg=msg id="pop3"></Popup><br/><br/>
            <div>
                <h3>SMS ALERT ACTIVATION</h3>
                <input type="checkbox" class="myCheck" v-on:click="activateSMS()"><br/><br/>
            </div>

        </div>
        <p><button class="save">Save</button></p>

    </div>
</template>

<script>
    import Popup from "@/components/Popup";

    export default {
        name: "Profile",
        components:{
            Popup
        },
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
                isActivated: false,
                usernameChange:'Change your username',
                title:"Change your personal data",
                msg:"Here you can change your personal data. In progress",
                title1:"Change phone number",
                msg1:"Here you can change your phone number",
                title2:"Change email address",
                msg2:"Here you can change your email address",

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

    #pop1, #pop2, #pop3{
        float: top;
    }
    #pop1{

    }
</style>
