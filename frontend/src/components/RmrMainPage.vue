<template>
    <div>
        <div class="header m-2">
            <TitleHeaderDashBoard></TitleHeaderDashBoard>
            <SignHeaderDashBoard></SignHeaderDashBoard>
            <ResultHeaderDashBoard></ResultHeaderDashBoard>
        </div>
        <ProductionLine></ProductionLine>
        <!-- <TableValue></TableValue> -->
    </div>
</template>

<script>
import TitleHeaderDashBoard from './TitleHeaderDashBoard.vue';
import SignHeaderDashBoard from './SignHeaderDashBoard.vue';
import ResultHeaderDashBoard from './ResultHeaderDashBoard.vue';
import ProductionLine from './ProductionLine.vue';
// import TableValue from './TableValue.vue';
export default {
    name: "RmrMainPage",
    components: {
        TitleHeaderDashBoard,
        SignHeaderDashBoard,
        ResultHeaderDashBoard,
        ProductionLine,
        // TableValue
    }
}
</script>

<style scoped>
.header {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto auto auto;
    grid-template-areas: 'Title' 'Sign' 'Result';

    border: 2px solid black;
}
</style>