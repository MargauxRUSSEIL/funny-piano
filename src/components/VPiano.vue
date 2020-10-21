<template>
    <div class="Piano">
        <div class="Piano__container m-auto flex flex-col">
            <div class="touches-blanches flex mt-3">
                <button ref="button" class="touche-blanche" @click="onClick"></button>
                <button ref="button" class="touche-blanche" @click="onClick"></button>
                <button class="touche-blanche" @click="onClick"></button>
                <button class="touche-blanche" @click="onClick"></button>
                <button class="touche-blanche" @click="onClick"></button>
                <button class="touche-blanche" @click="onClick"></button>
                <button class="touche-blanche" @click="onClick"></button>
            </div>
            <div class="touches-noires flex">
                <button class="touche-noire" @click="onClick"></button>
                <button class="touche-noire" @click="onClick"></button>
                <button class="touche-noire" @click="onClick"></button>
                <button class="touche-noire" @click="onClick"></button>
                <button class="touche-noire" @click="onClick"></button>
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
        onClick : function () {
            const noteDo = document.createElement('noteDo')
            noteDo.src = '@/public/asstes/sounds/A.mp3'

            noteDo.play()
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