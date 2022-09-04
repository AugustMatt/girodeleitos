<template>
    <div class="preloader">
        <img class="animation__shake" src="/icons/gohorse.png" height="120" width="100">
    </div>
</template>

<style>
    
    .preloader {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: #454d55;
        color: #fff;
        height: 100vh;
        width: 100vw;
        animation: scroolUp 1s 1.5s forwards, desapareca 1s 1.5s forwards;
        position: absolute;
        z-index: 9999;
    }

    @keyframes scroolUp {
        0% {
            max-height: 100vh;
        }
        100% {
            max-height: 0vh;
        }
    }

    .animation__shake {
        vertical-align: middle;
        border-style: none; 
        animation: shake 1.5s;
        background-color: white;
        border-radius: 30%;
    }

    @keyframes shake {
        0% {
            -webkit-transform: translate(2px, 1px) rotate(0);
            transform: translate(2px, 1px) rotate(0)
        }

        10% {
            -webkit-transform: translate(-1px, -2px) rotate(-2deg);
            transform: translate(-1px, -2px) rotate(-2deg)
        }

        20% {
            -webkit-transform: translate(-3px, 0) rotate(3deg);
            transform: translate(-3px, 0) rotate(3deg)
        }

        30% {
            -webkit-transform: translate(0, 2px) rotate(0);
            transform: translate(0, 2px) rotate(0)
        }

        40% {
            -webkit-transform: translate(1px, -1px) rotate(1deg);
            transform: translate(1px, -1px) rotate(1deg)
        }

        50% {
            -webkit-transform: translate(-1px, 2px) rotate(-1deg);
            transform: translate(-1px, 2px) rotate(-1deg)
        }

        60% {
            -webkit-transform: translate(-3px, 1px) rotate(0);
            transform: translate(-3px, 1px) rotate(0)
        }

        70% {
            -webkit-transform: translate(2px, 1px) rotate(-2deg);
            transform: translate(2px, 1px) rotate(-2deg)
        }

        80% {
            -webkit-transform: translate(-1px, -1px) rotate(4deg);
            transform: translate(-1px, -1px) rotate(4deg)
        }

        90% {
            -webkit-transform: translate(2px, 2px) rotate(0);
            transform: translate(2px, 2px) rotate(0)
        }

        100% {
            -webkit-transform: translate(1px, -2px) rotate(-1deg);
            transform: translate(1px, -2px) rotate(-1deg)
        }
    }

    @keyframes desapareca {
        0% {
            opacity: 1;
        }
        100% {
            opacity: 0;
        }
    }

    
</style>