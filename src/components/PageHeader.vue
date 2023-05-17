<template>
    <section>
        <header>
            <div class="header-menu">
                <a href="https://vdnh.ru/events/">События</a>
                <a href="https://vdnh.ru/visitors/?utm_source=button&utm_medium=banner&utm_campaign=vdnh_promo">Посетителям</a>
                <a href="https://vdnh.ru/selections/kupit-bilet/">Билеты</a>
                <a href="https://vdnh.ru/visitors/loyalty/?utm_source=site&utm_medium=menu&utm_campaign=privilegii">Скидки</a>
                <a href="https://vdnh.ru/news/">Новости</a>
                <a href="https://vdnh.ru/contacts/">Контакты</a>
            </div>  
        </header>
        <div class = "element-text">
            <h3>ВДНХ</h3>
            <h1 class="el">Выстовочно-торговый центр <br/>республики Казахстан</h1>            
        </div>
        <div :style = "image" class = "image"></div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                image: {backgroundImage: 'url(' + require('@/assets/pavilon.jpg') + ')'}
            };
        }
    };
</script>

<style scoped>
    header{
        background-color: rgb(221, 226, 226);
        position: fixed;
        z-index: 10;
        padding: 20px;
        min-width: 100vw;;
        min-height: 30px;
        opacity: 0.9;
        border-radius: 5px;
        box-shadow: 0 0 10px 2px;
        top: 1%;
    }

    a{
        display:inline-block;
        margin: 0px 62px 0 0;
        color: rgb(50, 50, 100);
        text-decoration: none;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    }

    .image {
        background-repeat: no-repeat;
        background-position: top;
        min-height: 90vh;
        filter: brightness(40%);
        background-size: cover;
        box-shadow: 0 0 20px 2px 
    }

    .element-text{
        position: absolute;
        left: 0;
        right: 0;
        top: 15vh;       
        color: #dddddd;
        z-index: 1;
    }


    h1{
        font-size: 4.5vmax;
        font-family: Georgia, 'Times New Roman', Times, serif;
    }

    h3{
        font-size: 1.5vmax;
        padding-bottom: 10vh;
    }
</style>