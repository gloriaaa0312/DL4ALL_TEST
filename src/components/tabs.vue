<template>
    <div class="tabs">
        <div class="tab_header">
            <button v-for="tab in tabs" :key="tab.idx" :class="{ active: activeTab === tab.idx }" @click="activeTab = tab.idx">{{ tab.title }}</button>
        </div>

        <div class="tab_content">
        <div v-if="activeTab === '1'">主页内容</div>
        <div v-if="activeTab === '2'">课程首页</div>
        <div v-if="activeTab === '3'">学习页面</div>
        </div>
    </div>
</template>

<script setup>
  import { ref } from 'vue';

  const activeTab = ref('1'); 

  const tabs=[
        {title:'主页',idx:'1'},
        {title:'课程',idx:'2'},
        {title:'学习',idx:'3'},
    ]
</script>


<style>
.tabs {
    font-family: 'Arial', sans-serif;
}

.tab_header {
    display: flex;
    border-bottom: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
}

.tab_header button {
    padding: 10px 20px;
    margin-right: 5px;
    border: none;
    background-color: #f0f0f0;
    cursor: pointer;
    transition: background-color 0.3s;
}

.tab_header button:hover {
    background-color: #e0e0e0;
}

.tab_header .active {
    background-color: #007bff;
    color: white;
}
</style>