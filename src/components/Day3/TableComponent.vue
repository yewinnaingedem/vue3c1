<template>
    <table class="table">
        <thead>
            <tr>
                <th v-for="column in table.columns" :key="column" scope="col">{{ column }}</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="row in table.rows " :key="row" >
                <td>{{ row.first }}</td>
                <td>{{ row.Last }}</td>
                <td>{{ row.age }}</td>
            </tr>
        </tbody>
    </table>
</template>

<script>
export default {
    name: "TableComponent",
    props : {
        table : Object ,
    }
}
</script>