<script>

export default {
    data() {
        return {
            questions: [
                {
                    question: "Qual è la capitale del Giappone?",
                    answers: [
                        "A: Tokyo",
                        "B: Pechino",
                        "C: Seul",
                        "D: Bangkok"
                    ]
                },
                {
                    question: "Quale è il fiume più lungo del mondo?",
                    answers: [
                        "A: Nilo",
                        "B: Amazonas",
                        "C: Mississippi",
                        "D: Yangtze"
                    ]
                },
                {
                    question: "In quale anno è stata firmata la Dichiarazione di Indipendenza degli Stati Uniti?",
                    answers: [
                        "A: 1776",
                        "B: 1789",
                        "C: 1812",
                        "D: 1865"
                    ]
                },
                {
                    question: "Chi era il primo imperatore romano?",
                    answers: [
                        "A: Augusto",
                        "B: Cesare",
                        "C: Nerone",
                        "D: Tiberio"
                    ]
                },
                {
                    question: "Qual è l'elemento chimico con simbolo H?",
                    answers: [
                        "A: Ossigeno",
                        "B: Idrogeno",
                        "C: Carbonio",
                        "D: Azoto"
                    ]
                },
                {
                    question: "Chi ha scoperto la legge di gravitazione universale?",
                    answers: [
                        "A: Galileo Galilei",
                        "B: Isaac Newton",
                        "C: Albert Einstein",
                        "D: Charles Darwin"
                    ]
                },
                {
                    question: "Qual è il quadro più famoso di Leonardo da Vinci?",
                    answers: [
                        "A: La Gioconda",
                        "B: L'Ultima Cena",
                        "C: Venere di Urbino",
                        "D: La Primavera"
                    ]
                },
                {
                    question: "Chi è l'autore del romanzo 'Il Piccolo Principe'?",
                    answers: [
                        "A: Antoine de Saint-Exupéry",
                        "B: Victor Hugo",
                        "C: Marcel Proust",
                        "D: Ernest Hemingway"
                    ]
                },
                {
                    question: "Chi è il primo ministro del Regno Unito?",
                    answers: [
                        "A: Boris Johnson",
                        "B: Angela Merkel",
                        "C: Emmanuel Macron",
                        "D: Justin Trudeau"
                    ]
                },
                {
                    question: "Quale presidente degli Stati Uniti ha servito per quattro mandati?",
                    answers: [
                        "A: Franklin D. Roosevelt",
                        "B: Abraham Lincoln",
                        "C: George Washington",
                        "D: Thomas Jefferson"
                    ]
                }
            ]
        }
    },
}
</script>

<!-- --------------------------------------------------------------------------------- -->

<template>
    <div id="main-template" class="text-light">
        <div class="my-box text-center fw-bold">
            <div class="bg-up py-5">
                <img src="https://i.pinimg.com/474x/80/f3/e7/80f3e71a6ce9ab46b027423d056cef94.jpg">
            </div>

            <div class="bg-down py-5" v-for="question in questions">
                <div class='content container'>
                    <!-- Question -->
                    <p class="borders fs-4 p-3">{{ question.question }}</p>
        
                    <!-- Answers -->
                    <div class="row">
                        <div v-for="answer in question.answers" class="col-md-6 col-sm-12">
                            <div class="my-card borders p-2 m-2">    
                                {{ answer }}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<!-- --------------------------------------------------------------------------------- -->

<style scoped>

    /* ---------------------------- */

    .my-card:hover{
        background-color: lightgray;
        cursor: pointer;
        color: black;
    }

    .bg-up {
        background-color: #11138C;
    }

    .bg-down {
        background-color: #11093A;
    }

    .borders{
        border: 1px solid white;
    }
</style>
