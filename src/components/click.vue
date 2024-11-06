<template>
<h2>内联事件处理</h2>
<button @click="ans++">+=1</button>
<p>cnt:{{ ans }}</p>

<h2>方法事件处理</h2>
<button @dblclick="cnt_test">+=1</button>
<p>cnt:{{ ans2 }}</p>

<h2>传参</h2>
<p @click="getName(item, $event)" v-for="(item,index) in names":key="index">{{ item }}</p>
</template>

<script>
export default{
    data(){
        return{
            ans:0,
            ans2:0,
            names:['12', '22', '32']
        }
    },
    methods:{
        cnt_test(){
            console.log('click');
            this.ans2 += 1;
        },
        getName(name, e){
            console.log(name)
            console.log(e)
        }
        
    }
}
</script>