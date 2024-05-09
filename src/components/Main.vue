<script>

export default {
    data() {
        return {
            questions: [
                {
                    id: 1,
                    question: "Qual è la capitale del Giappone?",
                    answers: [
                        { id: 1, text: "A: Tokyo" },
                        { id: 2, text: "B: Pechino" },
                        { id: 3, text: "C: Seul" },
                        { id: 4, text: "D: Bangkok" }
                    ],
                    right_answer: { id: 1, text: "A: Tokyo" }
                },
                {
                    id: 2,
                    question: "Quale è il fiume più lungo del mondo?",
                    answers: [
                        { id: 1, text: "A: Nilo" },
                        { id: 2, text: "B: Amazonas" },
                        { id: 3, text: "C: Mississippi" },
                        { id: 4, text: "D: Yangtze" }
                    ],
                    right_answer: { id: 2, text: "B: Amazonas" }
                },
                {
                    id: 3,
                    question: "In quale anno è stata firmata la Dichiarazione di Indipendenza degli Stati Uniti?",
                    answers: [
                        { id: 1, text: "A: 1776" },
                        { id: 2, text: "B: 1789" },
                        { id: 3, text: "C: 1812" },
                        { id: 4, text: "D: 1865" }
                    ],
                    right_answer: { id: 1, text: "A: 1776" }
                },
                {
                    id: 4,
                    question: "Chi era il primo imperatore romano?",
                    answers: [
                        { id: 1, text: "A: Augusto" },
                        { id: 2, text: "B: Cesare" },
                        { id: 3, text: "C: Nerone" },
                        { id: 4, text: "D: Tiberio" }
                    ],
                    right_answer: { id: 1, text: "A: Augusto" }
                },
                {
                    id: 5,
                    question: "Qual è l'elemento chimico con simbolo H?",
                    answers: [
                        { id: 1, text: "A: Ossigeno" },
                        { id: 2, text: "B: Idrogeno" },
                        { id: 3, text: "C: Carbonio" },
                        { id: 4, text: "D: Azoto" }
                    ],
                    right_answer: { id: 2, text: "B: Idrogeno" }
                },
                {
                    id: 6,
                    question: "Chi ha scoperto la legge di gravitazione universale?",
                    answers: [
                        { id: 1, text: "A: Galileo Galilei" },
                        { id: 2, text: "B: Isaac Newton" },
                        { id: 3, text: "C: Albert Einstein" },
                        { id: 4, text: "D: Charles Darwin" }
                    ],
                    right_answer: { id: 2, text: "B: Isaac Newton" }
                },
                {
                    id: 7,
                    question: "Qual è il quadro più famoso di Leonardo da Vinci?",
                    answers: [
                        { id: 1, text: "A: La Gioconda" },
                        { id: 2, text: "B: L'Ultima Cena" },
                        { id: 3, text: "C: Venere di Urbino" },
                        { id: 4, text: "D: La Primavera" }
                    ],
                    right_answer: { id: 1, text: "A: La Gioconda" }
                },
                {
                    id: 8,
                    question: "Chi è l'autore del romanzo 'Il Piccolo Principe'?",
                    answers: [
                        { id: 1, text: "A: Antoine de Saint-Exupéry" },
                        { id: 2, text: "B: Victor Hugo" },
                        { id: 3, text: "C: Marcel Proust" },
                        { id: 4, text: "D: Ernest Hemingway" }
                    ],
                    right_answer: { id: 1, text: "A: Antoine de Saint-Exupéry" }
                },
                {
                    id: 9,
                    question: "Chi è il primo ministro del Regno Unito?",
                    answers: [
                        { id: 1, text: "A: Boris Johnson" },
                        { id: 2, text: "B: Angela Merkel" },
                        { id: 3, text: "C: Emmanuel Macron" },
                        { id: 4, text: "D: Justin Trudeau" }
                    ],
                    right_answer: { id: 1, text: "A: Boris Johnson" }
                },
                {
                    id: 10,
                    question: "Quale presidente degli Stati Uniti ha servito per quattro mandati?",
                    answers: [
                        { id: 1, text: "A: Franklin D. Roosevelt" },
                        { id: 2, text: "B: Abraham Lincoln" },
                        { id: 3, text: "C: George Washington" },
                        { id: 4, text: "D: Thomas Jefferson" }
                    ],
                    right_answer: { id: 1, text: "A: Franklin D. Roosevelt" }
                }
            ]
        }
    },
    methods: {
        checkAnswer(id){
            
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
                            <div @click='checkAnswer(answer.id)' class="my-card borders p-2 m-2">    
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
