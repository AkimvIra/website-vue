<template>
    <div class="osnov">
        <div class="main">
            <div v-for="index in data" :key="index" class="news">
                <img :src="index" :alt="index">     
            </div>
        </div> 
    </div>

</template>

<script>
export default {
    data(){
        return{ 
            data: [         
                   require('../assets/1.jpg'),
                   require('../assets/2.jpg'),
                   require('../assets/3.jpg'),
                   require('../assets/4.jpg'),
                   require('../assets/5.jpg'),
            ]
        }
    }
}
</script>

<style scoped>
.main{
    display: flex;
    overflow-x: auto;
    cursor: ew-resize;
}

.main::-webkit-scrollbar{
    display: none;
}
.news{
    min-width: 40dvw;
    margin: 10px 5px 10px 5px;
    border-radius: 8px;
    box-shadow: 0px 5px 6px  rgba(0, 0, 0, 0.458);
}

img{
    float: right;
    border-radius: 8px;
    width: 100%;
    height: 100%;
}

</style>