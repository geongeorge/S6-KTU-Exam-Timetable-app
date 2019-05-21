<template>
    <div>
<v-layout>
<v-container>
    <div class="t-flex">
        <t-card  :day="true" num="Su"></t-card>
        <t-card  :day="true" num="Mo"></t-card>
        <t-card  :day="true" num="Tu"></t-card>
        <t-card  :day="true" num="We"></t-card>
        <t-card  :day="true" num="Th"></t-card>
        <t-card  :day="true" num="Fr"></t-card>
        <t-card  :day="true" num="Sa"></t-card>
    </div>
    <div class="t-flex">
        <t-card :today="today" v-for="(date,index) in dates1" :key="index" :num="date.day" :exm="date.exam"></t-card>
    </div>
    <div class="t-flex">
        <t-card :today="today" v-for="(date,index) in dates2" :key="index" :num="date.day" :exm="date.exam"></t-card>
    </div>
    <div class="t-flex">
        <t-card :today="today" v-for="(date,index) in dates3" :key="index" :num="date.day" :exm="date.exam"></t-card>
    </div>
    <div class="t-flex">
        <t-card :today="today" v-for="(date,index) in dates4" :key="index" :num="date.day" :exm="date.exam"></t-card>
    </div>
</v-container>
</v-layout>
    </div>
</template>

<script>
import TCard from './TCard'
export default {
    components: {
        TCard
    },
    data: () => ({
        dates1 : [],
        dates2 : [],
        dates3 : [],
        dates4 : [],
        today: 0
    }),
    methods: {

    },
    mounted() {
        this.dates1 =  [
            { day: 19, exam: "" },
            { day: 20, exam: "" },
            { day: 21, exam: "" },
            { day: 22, exam: "" },
            { day: 23, exam: "" },
            { day: 24, exam: "" },
            { day: 25, exam: "" },
        ];
        this.dates2 =  [
             { day: 26, exam: "" },
            { day: 27, exam: "Elec" },
            { day: 28, exam: "" },
            { day: 29, exam: "DAA" },
            { day: 30, exam: "" },
            { day: 31, exam: "CD" },
            { day: 1, exam: "" },
        ];
        this.dates3 =  [
            { day: 2, exam: "" },
            { day: 3, exam: "" },
            { day: 4, exam: "CN" },
            { day: 5, exam: "" },
            { day: 6, exam: "" },
            { day: 7, exam: "SEP" },
            { day: 8, exam: "" },
        ];
        this.dates4 =  [
            { day: 9, exam: "" },
            { day: 10, exam: "PM" },
            { day: 11, exam: "" },
            { day: 12, exam: "" },
            { day: 13, exam: "" },
            { day: 14, exam: "" },
            { day: 15, exam: "" },
        ];

        let tdy = new Date();
        this.today = String(tdy.getDate()).padStart(2, '0');
    }
}
</script>

<style>
.t-flex {
  display: flex;
  flex-wrap: nowrap;
}
</style>
