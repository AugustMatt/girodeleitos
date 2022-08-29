<script>

</script>

<template>
    
    <div class="openingScreen d-flex flex-column justify-content-center align-items-center">
        <h1 class="neonText">
            <span>Giro</span><br>
            <span>de</span><br>
            <span>Leitos</span>
        </h1>
        <img class="rotatingBed bed1" src="/images/bed1.jpg">
        <img class="rotatingBed bed2" src="/images/bed2.jpg">
        <img class="rotatingBed bed3" src="/images/bed3.jpg">
        <img class="rotatingBed bed4" src="/images/bed4.jpg">
        <img class="rotatingBed bed5" src="/images/bed5.jpg">
    </div>

</template>

<style>

    /* Efeito Neon para os textos com essa classe */
    .neonText {
        top: 71vh;
        left: 0vh;
        position: relative;
        color: #fff;
        text-align: center;
        font-weight: 400;
        font-size: 3.0rem;
        text-shadow:
            0 0 7px #fff,
            0 0 10px #fff,
            0 0 21px #fff;
    }

    /* Opacidade 0 para ocultar o elemento */
    span{
        opacity: 0;
    }

    /* Animação para cada span com o texto aparecer */
    span:nth-child(1) {
        animation: fade-in 0.8s 2.25s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    span:nth-child(3) {
        animation: fade-in 0.8s 2.75s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    span:nth-child(5) {
        animation: fade-in 0.8s 3.25s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    /* Opacidade 1 para exibir o elemento */
    @keyframes fade-in {
        100% {
            opacity: 1;
            filter: blur(0);
        }
    }

    /* Background da animação inicial */
    .openingScreen {
        overflow:hidden;
        height: 100vh;
        background: linear-gradient(to bottom, #f8f8f8 0%, #1d1bb1 100%);
        animation: openingScreen 1s 4.25s forwards;
    }

    /* Animação para o background */
    @keyframes openingScreen {
        0% {
            max-height: 100vh;
        }
        100% {
            max-height: 0;
        }
    }

    /* Animação para telas com 768 pixels de largura ou mais */
    @media screen and (min-width: 768px){
        
        .rotatingBed {
            height: 180px;
            width: 300px;
        }

        .bed1 {
            top: 5vh;
            left: 0vw;
            animation: fadingBed1 1s linear, rotatingBed1 1s linear 1.25s, shakeBed 1.5s linear 2.5s;
        }

        @keyframes fadingBed1 {
            0% {
                opacity: 0;
            }
            100% {
                top: 10vh;
                opacity: 1;
            }
        }

        @keyframes rotatingBed1 {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        .bed2 {
            top: 15vh;
            left: -35vw;
            animation: fadingBed2 1s linear, rotatingBed2 1s linear 1.25s, shakeBed 1.5s linear 2.5s;
        }

        @keyframes fadingBed2 {
            0% {
                opacity: 0;
            }
            100% {
                left: -25vw;
                opacity: 1;
            }
        }

        @keyframes rotatingBed2 {
            0% {
                transform: rotateX(0deg);
            }
            100% {
                transform: rotateX(360deg);
            }
        }

        .bed3 {
            top: 20vh;
            left: 25vw;
            animation: fadingBed3 1s linear, rotatingBed3 1s linear 1.25s, shakeBed 1.5s linear 2.5s;
        }

        @keyframes fadingBed3 {
            0% {
                left: -22vw;
                opacity: 0;
            }
            100% {
                left: -12vw;
                opacity: 1;
            }
        }

        @keyframes rotatingBed3 {
            0% {
                transform: rotateY(0deg);
            }
            100% {
                transform: rotateY(-360deg);
            }
        }

        .bed4 {
            top: -9vh;
            left: 23vw;
            animation: fadingBed4 1s linear, rotatingBed4 1s linear 1.25s, shakeBed 1.5s linear 2.5s;
        }

        @keyframes fadingBed4 {
            0% {
                opacity: 0;
            }
            100% {
                left: 13vw;
                opacity: 1;
            }
        }

        @keyframes rotatingBed4 {
            0% {
                transform: rotateY(0deg);
            }
            100% {
                transform: rotateY(360deg);
            }
        }

        .bed5 {
            top:-72vh;
            left: 35vw;
            animation: fadingBed5 1s linear, rotatingBed5 1s linear 1.25s, shakeBed 1s linear 2.5s;
        }

        @keyframes fadingBed5 {
            0% {
                opacity: 0;
            }   
            100% {
                left: 25vw;
                opacity: 1;
            }
        }

        @keyframes rotatingBed5 {
            0% {
                transform: rotateX(0deg);
            }
            100% {
                transform: rotateX(-360deg);
            }
        }

    }

    /* Animação para telas com menos de 768 pixels de largura */
    @media screen and (max-width: 767px){
        .rotatingBed {
            height: 90px;
            width: 150px;
        }
    }

    /* Imagem que rotacioona */
    .rotatingBed {
        position: relative;
        border-radius: 5%;
        animation-fill-mode: forwards;
    }
  
    /* Animação de tremor */
    @keyframes shakeBed {
        0% { transform: translate(1px, 1px) rotate(0deg); }
        50% { transform: translate(-1px, -1px) rotate(-1deg); }
        10% { transform: translate(-1px, -2px) rotate(-1deg); }
        15% { transform: translate(1px, -1px) rotate(1deg); }
        20% { transform: translate(-3px, 0px) rotate(1deg); }
        25% { transform: translate(1px, 2px) rotate(-1deg); }
        30% { transform: translate(3px, 2px) rotate(0deg); }
        35% { transform: translate(-1px, -1px) rotate(1deg); }
        40% { transform: translate(1px, -1px) rotate(1deg); }
        45% { transform: translate(-1px, 1px) rotate(0deg); }
        50% { transform: translate(-1px, 2px) rotate(-1deg); }
        55% { transform: translate(1px, 1px) rotate(1deg); }
        60% { transform: translate(-3px, 1px) rotate(0deg); }
        65% { transform: translate(1px, -1px) rotate(1deg); }
        70% { transform: translate(3px, 1px) rotate(-1deg); }
        75% { transform: translate(-1px, 1px) rotate(1deg); }
        80% { transform: translate(-1px, -1px) rotate(1deg); }
        85% { transform: translate(1px, 1px) rotate(0deg); }
        90% { transform: translate(1px, 2px) rotate(0deg); }
        95% { transform: translate(-1px, -1px) rotate(1deg); }
        100% { transform: translate(1px, -2px) rotate(-1deg); }
    }

    


</style>