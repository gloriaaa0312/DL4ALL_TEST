<template>
    <h3>列表渲染</h3>
    <p v-for="item in names">{{ item }}</p>
</template>

<script>
export default{
    data(){
        return{
            names:['fyy', 'xrq', 'cvo', 'qunyou']
        }
    }
}
</script>