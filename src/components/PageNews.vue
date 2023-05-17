<template>
    <div class="main">
        <div v-for="index in data" :key="index.id" class="news">
            <div class="heading"> {{ index.head }}   
                <div class="tupe">{{ index.tupe }}</div>
                <img :src="index.img" :style="{width: '30%', height: '30%'}"/> 
            </div>
            <a v-bind:href="index.link">{{ index.name }}</a> 
            <div class="time">{{ index.time }}</div>     
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{ 
            data: [ 
                {
                    head: 'Сбытия на этой площадке:',
                    tupe: 'Концерты и шоу',
                    name: 'Шоу-сказка "Тайна Лунозавра',
                    link: 'https://vdnh.ru/events/shou-skazka-tayna-lunozavra/',
                    img:  'https://vdnh.ru/upload/iblock/424/4243385af874f356a3fb117face5b1b8.jpeg',
                    time: '27 мая, 11:00'
                },
                
                {
                    head: 'Сбытия на этой площадке:',
                    tupe: 'Комбо-программа',
                    name: 'Интерактивная экспозиция',
                    link: 'https://vdnh.ru/events/prazdnik-nauryz-v-pavilone-kazakhstan/?utm_source=vk&utm_medium=social&utm_campaign=fun&utm_content=prazdnik-nauryz-v-pavilone-kazakhstan',
                    img:  'https://vdnh.ru/upload/resize_cache/iblock/1b9/1000_424_1/1b9943c55421e93b094679b7216d730e.jpg',
                    time: 'В рабочие дни, с 12:30 до 20:00'
                }
            ]
        }
    }
}
</script>

<style scoped>
.main{
    display: block;
    width: 100%;
    max-width: 1024px;
    margin: 20px auto 10px auto;
    background-color: #ffffff00;
}

.news{
    display: inline-block;
    width: 90%;
    max-width: 400px;
    margin: 10px 15px 10px 15px;
    padding: 10px 0 5px 0;
    border-radius: 8px;
    box-shadow: 0px 5px 6px  rgba(0, 0, 0, 0.458);
    background-color: #c1c1c1;
}

.heading{
    font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: large;
    font-weight: 700;
    text-align: left;
    margin-left: 20px;
}

.tupe{
    font-weight: 300;
    font-size: medium;
    color: blue;
    margin: 5px 20px 15px;
}

a{
    color: #000;
    margin: 0 10px 0 10px;
}

img{
    float: right;
    margin-right: 10px;
    border-radius: 8px;
}

.time{
    text-align: left;
    margin: 20px 20px;
}
</style>