<template>
    <div class="Piano">
        <div class="Piano__container m-auto flex flex-col">
            <div class="touches-blanches flex lg:mt-3 mt-2 ;">
                <button class="touche-blanche" @click="playAudio('/assets/sounds/C.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/D.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/E.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/F.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/G.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/A.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/B.mp3')"></button>
            </div>
            <div class="touches-noires flex">
                <button class="touche-noire" @click="playAudio('/assets/sounds/C%23.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/D%23.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/F%23.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/G%23.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/A%23.mp3')"></button>
            </div>
            
        </div>
        <div class="Notes__container m-auto hidden md:flex">
            <p class="note">Do</p>
            <p class="note">Ré</p>
            <p class="note">Mi</p>
            <p class="note">Fa</p>
            <p class="note">Sol</p>
            <p class="note">La</p>
            <p class="note">Si</p>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        playAudio : function (url) {
            new Audio(url).play() ;
        }
    }
}
</script>

<style lang="postcss" scoped>

@media only screen and (max-width: 767px) {
    .Piano {
        padding-bottom: 35px;
    }
}

.Piano__container {
    height: 276px ;
    width: 531px ;
    border-radius: 10px ;
    background: black ;
    margin-bottom: 40px ;
    align-items: center ;
    box-shadow: 1px 1px 30px rgb(97, 47, 47) ;
}

@media only screen and (max-width: 767px) {
    .Piano__container {
        max-height: 190px ;
        max-width: 368px ;
        margin-top: 180px ;
    }
}

.touche-blanche:nth-child(1) {
    height: 252px ;
    width: 69px ;
    background: #FFFFFF ;
    border-radius: 5px 0px 0px 5px ;
}

@media only screen and (max-width: 767px) {
    .touche-blanche:nth-child(1) {
        height: 173px ;
        width: 47px ;
    }
}

.touche-blanche:nth-child(7) {
    height: 252px ;
    width: 69px ; 
    background: #FFFFFF ; 
    border-radius: 0px 5px 5px 0px ;
}

@media only screen and (max-width: 767px) {
    .touche-blanche:nth-child(7) {
        height: 173px ;
        width: 47px ;  
    }
}

.touche-blanche {
    height: 252px ;
    width: 69px ;
    background: #FFFFFF ;
    margin: 0px 2px ;
}

@media only screen and (max-width: 767px) {
    .touche-blanche {
        height: 173px ;
        width: 47px ;
    }
}

.touche-blanche:focus {
    background: #FFD12D ;
}

.touches-noires {
    width: 507px ;
    margin-top: -252px ;
    align-items: flex-start ;
}

@media only screen and (max-width: 767px) {
    .touches-noires {
        width: 368px ;
        margin-top: -175px ;
    }
}

.touche-noire {
    height: 184px ;
    width: 30px ;
    background: #000000 ;
    border-radius: 0px 0px 5px 5px ;
    margin-left: 43px ;
}

@media only screen and (max-width: 767px) {
    .touche-noire {
        height: 126px ;
        width: 21px ;
        margin-left: 30px ;
    }
}

.touche-noire:focus {
    background: #E6016F ;
}

.touche-noire:nth-child(1) {
    margin-left: 56px ;
}

@media only screen and (max-width: 767px) {
    .touche-noire:nth-child(1) {
        margin-left: 46px ;
    }
}

.touche-noire:nth-child(2) {
    margin-right: 73px ;
}

@media only screen and (max-width: 767px) {
    .touche-noire:nth-child(2) {
        margin-right: 50px ;
    }
}

.Notes__container {
    width: 531px ;
    justify-content: center ;
    padding-bottom: 34px;
}
.note {
    text-transform: uppercase ;
    width: 73px ;
    color: rgba(255, 255, 255, 0.4) ;
}
</style>