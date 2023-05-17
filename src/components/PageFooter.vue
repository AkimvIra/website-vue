<template>
    <footer>
        <div class="footer-menu">
            <img src="https://vdnh.ru/local/templates/v3_new_header/images/vue/logo-main.svg">
            <div class="menu">
                <a href="https://vdnh.ru/events/">События</a>
                <a href="https://vdnh.ru/visitors/?utm_source=button&utm_medium=banner&utm_campaign=vdnh_promo">Посетителям</a>
                <a href="https://vdnh.ru/selections/kupit-bilet/">Билеты</a>
                <a href="https://vdnh.ru/visitors/loyalty/?utm_source=site&utm_medium=menu&utm_campaign=privilegii">Скидки</a>
                <a href="https://vdnh.ru/news/">Новости</a>
                <a href="https://vdnh.ru/contacts/">Контакты</a>
            </div>
        </div>
  
    </footer>
</template>

<script>
export default {
    data(){
        return{ 

        }
    }
}
</script>

<style scoped>
    .footer-menu{
        padding-top: 30px;
        background-color: rgb(50, 50, 100);
        min-width: 100%;;
        min-height: 150px;
        box-shadow: 0 0 5px 2px;
    }

    img{
        filter:invert()
    }

    a{
        display:inline-block;
        margin: 15px 20px 5px 20px;
        color: rgb(232, 232, 232);
        text-decoration: none;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    }
</style>