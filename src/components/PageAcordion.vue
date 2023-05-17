<template>
    <div class = "acord">
        <PageFAQ v-for="(acord, i) in acord" 
        :acord = "acord" 
        :index="i" 
        :key="i"
        :open="acord.open"
        @toggleOpen="toggleOpen"/>
    </div>
</template>

<script>
import PageFAQ from './PageFAQ.vue';
export default {
    components: {
        PageFAQ
    },
    data() {
        return {
            acord: [
                {
                    question: "Контакты:",
                    answer1: "Телефон: +7(495)544-34-00",
                    answer2: "E-mail: info@vdnh.ru",
                    answer3: "проспект Мира, 119, павильон №11",
                    open: false
                },

                {
                    question: "Режим работы:",
                    answer1: "Ежедневно: 11:00 - 20:00",
                    open: false
                },
            ]
        }
    },
    methods: {
        toggleOpen: function (index) {
            this.acord = this.acord.map((acord, i) => {
                if(index === i) {
                    acord.open =! acord.open;
                }else{
                    acord.open = false;
                }
                return acord;
            });
        }
    }
}
</script>

<style>
.acord{
    display: block;
    width: 100%;
    max-width: 1024px;
    margin: 20px auto 20px auto;
    border-radius: 8px;
    box-shadow: 0px 0px 10px  rgba(0, 0, 0, 0.2);
    background-color: #fff;
}

.acord .question {
    position: relative;
    color: #3c3c3c;
    padding: 10px;
    font-size: 20px;
    font-weight: 700;
    font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    transition: all 0.2s linear;
    cursor: pointer;
}

.acord .question::after {
    content: '';

    position: absolute;
    top: 50%;
    right: 0px;
    transform: translateY(-50%) rotate(0deg);
    
    width: 30px;
    height: 30px;
    background-image: url('../down.ico');
    background-position: center;
    background-size: contain;
    background-repeat: no-repeat;

    transition: all 0.4s ease-in-out;
}

.acord.open .question{
    margin-bottom: 15px;
}

.acord.open .question::after{
    transform: translateY(-50%) rotate(90deg);
}

.acord .answer {
    color: #3c3c3c;
    font-size: 18px;
    opacity: 0;
    max-height: 0px;
    overflow-y: hidden;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    transition: all 0.5s ease-in-out;
}

.acord.open .answer{
    opacity: 1;
    background-color: hsl(0, 0%, 87%);
    max-height: 1000px;
}
</style>