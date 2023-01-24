<template>
    <div>
        <h1>Olá Life!</h1>
        <table>
            <tr v-for="line in grid" :key="line">
                <td v-for="cell in line" :key="cell" :class="{vivo: cell==1}"></td>
                <td></td>
            </tr>
        </table>
    </div>    
</template>

<script>
export default({
    name: 'Life',
    data() {
        return{
            grid: [
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,1,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0],
            ]
        }        
    },
})
</script>

<style>
table, th, td{
    border: 1px solid;
}
td {
    width: 30px;
    height: 30px;
}
.vivo{
    background-color: yellow;
}
</style>