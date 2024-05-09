<script>

export default {
    data() {
        return {
            questions: [
                {
                    question: "Qual è il fiume più lungo d'Italia?",
                    answers: [
                        "A: Po",
                        "B: Ticino",
                        "C: Tevere",
                        "D: Adige"
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
        <div class="bg-up"></div>

        <div class="my-box text-center fw-bold">
            <img class="mb-5" src="https://i.pinimg.com/474x/80/f3/e7/80f3e71a6ce9ab46b027423d056cef94.jpg">

            <!-- Question -->
            <p class="borders fs-4 mt-5 p-4">Domanda numero 1</p>

            <!-- Answers -->
            <div class="row">
                <div class="col-md-6 col-sm-12">
                    <div class="borders m-2">    
                        1
                    </div>
                </div>

                <div class="col-md-6 col-sm-12">
                    <div class="borders m-2">    
                        2
                    </div>
                </div>

                <div class="col-md-6 col-sm-12">
                    <div class="borders m-2">    
                        3
                    </div>
                </div>

                <div class="col-md-6 col-sm-12">
                    <div class="borders m-2">    
                        4
                    </div>
                </div>
            </div>
        </div>
        
        <div class="bg-down"></div>
    </div>
</template>

<!-- --------------------------------------------------------------------------------- -->

<style scoped>
    #main-template {
        height: 100vh;
        position: relative;
    }

    .bg-up {
        height: 45%;
        background-color: #181989;
    }

    .bg-down {
        height: 55%;
        background-color: #11093A;
    }

    .my-box {
        position: absolute;
        width: 70%;
        min-width: 500px;
        top: 5%;
        left: 15%;
    }

    .borders{
        border: 1px solid white;
    }
</style>
