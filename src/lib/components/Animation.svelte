<div class="wrapper">
    <div class="round"></div>
    <div class="round purple"></div>
    <div class="round"></div>
    <div class="round purple"></div>
    <div class="round"></div>
    <div class="round white"></div>
    <div class="round"></div>
    <div class="round white"></div>
    <div class="round"></div>
    <div class="round"></div>
    <div class="round black"></div>
    <div class="round black"></div>
    <div class="round"></div>
    <div class="round"></div>
</div>

<style>
    .wrapper {
        top: -30px;
        position: absolute;
        width: 100%;
        height: 100%;
        z-index: -1;
        pointer-events: none;
    }
    .round {
        position: absolute;
        width: 10px;
        height: 10px;
        transform: rotate(90deg);
        background-color: var(--blue);
        border: 5px solid var(--blue);
        opacity: 0;
        box-shadow: 0 0 100px var(--blue), 0 0 10px var(--blue), 0 0 20px var(--blue);
        animation: animate 10s linear infinite, ani-2 5s linear infinite;
    }
    .purple{
    background-color: var(--purple);
    border: 5px solid var(--purple);
    box-shadow: 0 0 100px var(--purple), 0 0 10px var(--purple), 0 0 20px var(--purple);
    }
    .white{
    background-color: var(--white);
    border: 5px solid var(--white);
    box-shadow: 0 0 100px var(--white), 0 0 10px var(--white), 0 0 20px var(--white);
    }
    .black{
    background-color: var(--black);
    border: 5px solid var(--black);
    box-shadow: 0 0 100px var(--black), 0 0 10px var(--black), 0 0 20px var(--black);
    }
    .round:nth-child(1) {
        left: 5%;
        animation-delay: 0.5s;
    }
    .round:nth-child(2) {
        left: 65%;
        animation-delay: 1s;
    }
    .round:nth-child(3) {
        left: 90%;
        animation-delay: 1.5s;
    }
    .round:nth-child(4) {
        left: 18%;
        animation-delay: 2s;
    }
    .round:nth-child(5) {
        left: 93%;
        animation-delay: 2.5s;
    }
    .round:nth-child(6) {
        left: 52%;
        animation-delay: 3s;
    }
    .round:nth-child(7) {
        left: 65%;
        animation-delay: 3.5s;
    }
    .round:nth-child(8) {
        left: 35%;
        animation-delay: 4s;
    }
    .round:nth-child(9) {
        left: 85%;
        animation-delay: 4.5s;
    }
    .round:nth-child(10) {
        left: 45%;
        animation-delay: 5s;
    }
    .round:nth-child(11) {
        left: 36%;
        animation-delay: 5.5s;
    }
    .round:nth-child(12) {
        left: 72%;
        animation-delay: 6s;
    }
    .round:nth-child(13) {
        left: 14%;
        animation-delay: 6.5s;
    }
    .round:nth-child(14) {
        left: 70%;
        animation-delay: 7s;
    }
    @keyframes animate {
        0% {
            top: 0;
            opacity: 1;
        }
        20% {
            top: 20%;
            opacity: 0.8;
        }
        40% {
            top: 40%;
            opacity: 0.6;
        }
        60% {
            top: 60%;
            opacity: 0.4;
        }
        80% {
            top: 80%;
            opacity: 0.2;
        }
        100% {
            top: 100%;
            opacity: 0;
        }
    }
    @keyframes ani-2 {
        0%, 100% {
            transform: scale(1) rotate(40deg);
        }
        50% {
            transform: scale(2.5) rotate(40deg);
        }
    }
</style>