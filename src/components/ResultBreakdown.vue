<script setup>
import data from "../data/items.json"
</script>

<template>
    <div class="result-breakdown">
        <h5>Summary</h5>
        <div v-for="item in data" :key="item.id" class="breakdown-item" :style="{ backgroundColor: item.bgColor }">
            <div class="start">
                <img :src="item.icon" alt="">
                <h6 :style="{ color: item.color }">{{ item.tag }}</h6>
            </div>
            <div class="end">
                <h6 class="item-score">{{ item.score }}</h6>
                <p>/</p>
                <h6 class="item-benchmark">{{ item.benchmark }}</h6>
            </div>
        </div>
        <div class="continue">
            <h2>Continue</h2>
        </div>
    </div>
</template>

<style scoped>
.result-breakdown {
    padding: 0 30px 0 30px;
}

.result-breakdown h5 {
    margin-top: 20px;
    margin-bottom: 20px;
    color: hsl(224, 30%, 27%);
    font-size: 20px;
    font-weight: 800;
}

.breakdown-item {
    width: 100%;
    height: 60px;
    background-color: hsla(0, 100%, 67%, 0.1);
    border-radius: 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px 0 20px;
    margin-bottom: 20px;
}

.start {
    display: flex;
    align-items: center;
}

.start img {
    margin-right: 10px;
}

.start h6 {
    font-weight: 700;
    color: hsl(0, 100%, 67%);
    font-size: 18px;
}

.end {
    display: flex;
    align-items: center;
}

.end p {
    font-weight: 700;
    font-size: 18px;
    color: hsla(224, 30%, 27%, 0.4);
    margin-left: 5px;
    margin-right: 5px;
}

.item-score {
    font-weight: 800;
    font-size: 18px;
    color: hsl(224, 30%, 27%);
}

.item-benchmark {
    font-weight: 800;
    font-size: 18px;
    color: hsla(224, 30%, 27%, 0.4);
}

.continue {
    margin-top: 40px;
    margin-bottom: 20px;
    width: 100%;
    height: 70px;
    border-radius: 60px;
    background-color: hsl(224, 30%, 27%);
    display: flex;
    align-items: center;
    justify-content: center;
}

.continue h2 {
    color: hsl(0, 0%, 100%);
    font-weight: 700;
    font-style: 18px;
}

@media only screen and (min-width: 768px) {
    .result-breakdown {
        width: 50%;
        height: 100%;
    }

    .continue {
        height: 50px;
    }
    
}
</style>