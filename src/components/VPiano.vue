<template>
    <div class="Piano">
        <div class="Piano__container m-auto flex flex-col">
            <div class="touches-blanches flex mt-3">
                <button class="touche-blanche" @click="playAudio('/assets/sounds/C.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/D.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/E.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/F.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/G.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/A.mp3')"></button>
                <button class="touche-blanche" @click="playAudio('/assets/sounds/B.mp3')"></button>
            </div>
            <div class="touches-noires flex">
                <button class="touche-noire" @click="playAudio('/assets/sounds/Cc.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/Dd.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/Ff.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/Gg.mp3')"></button>
                <button class="touche-noire" @click="playAudio('/assets/sounds/Aa.mp3')"></button>
            </div>
            
        </div>
        <div class="Notes__container m-auto flex">
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
.Piano__container {
    height: 276px ;
    width: 531px ;
    border-radius: 10px ;
    background: black ;
    margin-bottom: 40px ;
    align-items: center ;
}
.touche-blanche:nth-child(1) {
    height: 252px ;
    width: 69px ;
    background: #FFFFFF ;
    border-radius: 5px 0px 0px 5px ;
}
.touche-blanche:nth-child(7) {
    height: 252px ;
    width: 69px ;
    background: #FFFFFF ; 
    border-radius: 0px 5px 5px 0px ; 
}
.touche-blanche {
    height: 252px ;
    width: 69px ;
    background: #FFFFFF ;
    margin: 0px 2px ;
}
.touche-blanche:focus {
    background: #FFD12D ;
}
.touches-noires {
    width: 507px ;
    margin-top: -252px ;
    align-items: flex-start ;
}
.touche-noire {
    height: 184px ;
    width: 30px ;
    background: #000000 ;
    border-radius: 0px 0px 5px 5px ;
    margin-left: 43px ;
}
.touche-noire:focus {
    background: #E6016F ;
}
.touche-noire:nth-child(1) {
    margin-left: 56px ;
}
.touche-noire:nth-child(2) {
    margin-right: 73px ;
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