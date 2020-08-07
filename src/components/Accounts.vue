<template>
    <div class="card">

        <div class="text">
            <h1>My Accounts</h1>
            <div class="accounts">
                <AccountButton></AccountButton>
                <p>6572 0932 2263 7773</p>
                <AccountButton></AccountButton>
                <p>5453 3382 0002 4382</p>
            </div>

        </div>
        <p><button class="save">Save</button></p>

    </div>
</template>

<script>
    import AccountButton from "@/components/AccountButton";
    export default {
        name: "Accounts",
        components:{AccountButton},

    }
</script>

<style scoped>
    h1{
        box-shadow: inset 0 0px 0 white, inset 0 -1px 0 rgba(40,40,40,0.29);

    }
    .text{
        font-family: Dosis, sans-serif;
        margin: 20px 30px;
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
    button:hover, a:hover {
        opacity: 0.7;
    }

</style>
