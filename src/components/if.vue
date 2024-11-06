<template>
<h3>条件渲染</h3>
<div v-if="flag">True</div>
<div v-else>false</div>
<div v-if="tyoe =='A'">A</div>
<div v-else-if="type == 'B'">B</div>
<div v-else>D</div>
</template>

<script>
export default{
    data(){
        return {
            flag:false,
            type:'B'
        }
    }
}
</script>