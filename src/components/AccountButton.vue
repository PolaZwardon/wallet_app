<template>
    <div>
        <h3>{{account_status}}</h3><button type="button" class="account_button" v-on:click="changeAccountStatus()">{{button_status}}</button>
    </div>
</template>

<script>
    export default {
        name: "AccountButton",
        methods: {
            changeAccountStatus: function () {
                if (this.account_status === "Blocked Account") {
                    this.account_status = "Active Account";
                    this.button_status = "Block Account";
                } else if (this.account_status === "Active Account") {
                    this.account_status = "Blocked Account";
                    this.button_status = "Activate Account";
                }
            }
        },
        data() {
            return {
                account_status: "Blocked Account",
                button_status: "Unblock Account"
            }
        }
    }
</script>

<style scoped>
    .account_button{
        border: none;
        outline: 0;
        display: inline-block;
        padding: 1px;
        color: white;
        background-color: rgba(40,40,40,0.89);
        text-align: center;
        cursor: pointer;
        width: 30%;
        font-size: 13px;
        float: right;
    }
</style>
