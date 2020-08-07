<template>
    <div class="card">

        <div class="text">
            <h1>My Bills</h1>

            <div>
                <p class="bill1">Phone Bill</p>
                <p class="bill2">Internet Bill</p>
                <p class="bill3">House Rent</p>
                <p class="bill4">Income Tax</p>

            </div>

        </div>

    </div>
</template>


<script>
    export default {
        name: "Bills"
    }
</script>

<style scoped>
    h1{
        box-shadow: inset 0 0px 0 white, inset 0 -1px 0 rgba(40,40,40,0.29);

    }
    .card {
        background: rgba(255,255,255,0.74);
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        max-width: 600px;
        margin: auto;
    }
    .text{
        font-family: Dosis, sans-serif;
        margin-left: 30px;
        margin-top: 20px;
        margin-bottom: 20px;
    }

</style>
