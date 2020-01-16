<template>
   <div class="search-bar">
        <div class="button">
            <span v-for="(item,index) in ['新闻','体育','娱乐']" :key="index" 
            @click="change(index)" :class="{active:current=index}">{{item}}</span>
        </div>

        <div v-if="current===0">
            <ul>
                <li>伊朗</li>
                <li>伊朗</li>
                <li>伊朗</li>
                
            </ul>
        </div>
        <div v-if="current===1">
            <ul>
                <li>国足</li>
                <li>国足</li>
                <li>国足</li>
                
            </ul>
        </div>
        <div v-if="current===2">
            <ul>
                <li>电影</li>
                <li>电影</li>
                <li>电影</li>    
            </ul>
        </div>
   </div>
</template>

<script>
export default {
    data(){
        return{
            current:0
        }
    },
    methods: {
        change(index){
            this.active=index
        }
    }

}
</script>

<style>
.active{
    color:red;
}
</style>