<template>
    <div :class="{
        'day': this.day,
        'today': this.today ==this.num
        }">
        {{num}}
        <span class="exam-title">{{exm}}</span>
    </div>
</template>

<script>
export default {
    props: {
        day : {default: false},
        today: {default: -1},
        num: {default: ''},
        exm: {default: ''}
    }
}
</script>

<style scoped>
div {
    border: 1px solid rgba(7, 164, 255, 0.2);
    border-radius: 2px;
    width: 100px;
    height: 80px;
    text-align: center;
    font-size: 1.5em;
    margin: 2px;
    padding: 2px;
}
.today {
    background-color: rgba(7, 164, 255, 0.2);
}
.exam-title {
    display: block;
    height: auto;
    text-align: center;
    font-size: 0.8em;
    color: rgb(231, 255, 195);
     background-color: rgba(7, 255, 81, 0.2);
    margin-bottom: auto;
}
.day {
    border: 0;
    height: auto;
    color:lightskyblue;
}
</style>
