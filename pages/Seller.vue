<template>
    <div class="seller-container">
<h1 class="header-doctors">Your Appointments</h1>
<Table/>
    </div>
</template>

<script>
import Table from "../components/Table.vue";
    export default {
    components: { Table }
}
</script>

<style  scoped>
.seller-container{
    min-height: 90vh;
}
</style>