<script>

export default {
    data() {
        return {
            questions: [
                {
                    id: 1,
                    question: "Qual è la capitale del Giappone?",
                    answers: [
                        { id: 1, text: "A: Tokyo", correct: true },
                        { id: 2, text: "B: Pechino", correct: false },
                        { id: 3, text: "C: Seul", correct: false },
                        { id: 4, text: "D: Bangkok", correct: false }
                    ]
                },
                {
                    id: 2,
                    question: "Quale è il fiume più lungo del mondo?",
                    answers: [
                        { id: 1, text: "A: Nilo", correct: false },
                        { id: 2, text: "B: Amazonas", correct: true },
                        { id: 3, text: "C: Mississippi", correct: false },
                        { id: 4, text: "D: Yangtze", correct: false }
                    ]
                },
                {
                    id: 3,
                    question: "In quale anno è stata firmata la Dichiarazione di Indipendenza degli Stati Uniti?",
                    answers: [
                        { id: 1, text: "A: 1776", correct: true },
                        { id: 2, text: "B: 1789", correct: false },
                        { id: 3, text: "C: 1812", correct: false },
                        { id: 4, text: "D: 1865", correct: false }
                    ]
                },
                {
                    id: 4,
                    question: "Chi era il primo imperatore romano?",
                    answers: [
                        { id: 1, text: "A: Augusto", correct: true },
                        { id: 2, text: "B: Cesare", correct: false },
                        { id: 3, text: "C: Nerone", correct: false },
                        { id: 4, text: "D: Tiberio", correct: false }
                    ]
                },
                {
                    id: 5,
                    question: "Qual è l'elemento chimico con simbolo H?",
                    answers: [
                        { id: 1, text: "A: Ossigeno", correct: false },
                        { id: 2, text: "B: Idrogeno", correct: true },
                        { id: 3, text: "C: Carbonio", correct: false },
                        { id: 4, text: "D: Azoto", correct: false }
                    ]
                },
                {
                    id: 6,
                    question: "Chi ha scoperto la legge di gravitazione universale?",
                    answers: [
                        { id: 1, text: "A: Galileo Galilei", correct: false },
                        { id: 2, text: "B: Isaac Newton", correct: true },
                        { id: 3, text: "C: Albert Einstein", correct: false },
                        { id: 4, text: "D: Charles Darwin", correct: false }
                    ]
                },
                {
                    id: 7,
                    question: "Qual è il quadro più famoso di Leonardo da Vinci?",
                    answers: [
                        { id: 1, text: "A: La Gioconda", correct: true },
                        { id: 2, text: "B: L'Ultima Cena", correct: false },
                        { id: 3, text: "C: Venere di Urbino", correct: false },
                        { id: 4, text: "D: La Primavera", correct: false }
                    ]
                },
                {
                    id: 8,
                    question: "Chi è l'autore del romanzo 'Il Piccolo Principe'?",
                    answers: [
                        { id: 1, text: "A: Antoine de Saint-Exupéry", correct: true },
                        { id: 2, text: "B: Victor Hugo", correct: false },
                        { id: 3, text: "C: Marcel Proust", correct: false },
                        { id: 4, text: "D: Ernest Hemingway", correct: false }
                    ]
                },
                {
                    id: 9,
                    question: "Chi è il primo ministro del Regno Unito?",
                    answers: [
                        { id: 1, text: "A: Boris Johnson", correct: true },
                        { id: 2, text: "B: Angela Merkel", correct: false },
                        { id: 3, text: "C: Emmanuel Macron", correct: false },
                        { id: 4, text: "D: Justin Trudeau", correct: false }
                    ]
                },
                {
                    id: 10,
                    question: "Quale presidente degli Stati Uniti ha servito per quattro mandati?",
                    answers: [
                        { id: 1, text: "A: Franklin D. Roosevelt", correct: true },
                        { id: 2, text: "B: Abraham Lincoln", correct: false },
                        { id: 3, text: "C: George Washington", correct: false },
                        { id: 4, text: "D: Thomas Jefferson", correct: false }
                    ]
                }
            ]
        }
    },
    methods: {
        checkAnswer(answer){
            if (answer.correct === true) {
                alert('Risposta corretta!');
            } else {
                alert('Risposta sbagliata!');
            }
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
                            <div @click='checkAnswer(answer)' class="my-card borders p-2 m-2">    
                                {{ answer.text }}
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
