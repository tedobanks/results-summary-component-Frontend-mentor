<template>
    <div class="result-info">
        <h5 class="title">Your Result</h5>
        <div class="score-circle">
            <h2>76</h2>
            <h5>of 100</h5>
        </div>
        <h4 class="remark-title">Great</h4>
        <p class="remark-body">You scored higher than 65% of the people who have taken these tests.</p>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@500;700;800&display=swap');
.result-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    height: 380px;
    background-image: linear-gradient(hsl(252, 100%, 67%), hsl(241, 81%, 54%));
    border-bottom-left-radius: 40px;
    border-bottom-right-radius: 40px;
}

.title {
    font-family: 'Hanken Grotesk', sans-serif;
    font-size: 22px;
    font-weight: 500;
    color: hsl(241, 100%, 89%);
    margin-top: 20px;
    margin-bottom: 20px;
}

.score-circle {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 150px;
    width: 150px;
    border-radius: 50%;
    background-image: linear-gradient(hsla(256, 72%, 46%, 1), hsla(241, 72%, 46%, 0));
}

.score-circle h2 {
    color: hsl(0, 0%, 100%);
    font-weight: 800;
    font-size: 60px;
    margin: 0;
    margin-top: 10px;
    padding: 0;
    line-height: 1.2;
}

.score-circle h5 {
    font-weight: 700;
    color: hsla(241, 100%, 89%, 0.7);
    font-size: 18px;
}

.remark-title {
    font-size: 30px;
    color: hsl(0, 0%, 100%);
    font-weight: 700;
    line-height: 1;
    margin-top: 30px;
    margin-bottom: 10px;
}

.remark-body {
    color: hsl(241, 100%, 89%);
    font-size: 18px;
    font-weight: 500;
    text-align: center;
    line-height: 1.2;
    padding-left: 30px;
    padding-right: 30px;
}
@media only screen and (min-width: 396px) and (max-width: 540px) {
    .remark-body{
        padding-left: 40px;
        padding-right: 40px;
    }
}
@media only screen and (min-width: 768px) {
    .result-info {
        width: 50%;
        height: 100%;
        border-radius: 40px;   
    }

    .title {
        margin-top: 30px;
        margin-bottom: 30px;
    }

    .score-circle{
        width: 200px;
        height: 200px;
    }
    .remark-title{
        margin-top: 40px;
        margin-bottom: 20px;
    }
    .remark-body{
        padding-left: 45px;
        padding-right: 45px;
    }
}
</style>