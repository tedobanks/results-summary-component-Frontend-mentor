<script setup>
import ResultInfo from "../components/ResultInfo.vue";
import ResultBreakdown from "../components/ResultBreakdown.vue"

</script>
<template>
    <section>
        <div class="container">
            <ResultInfo />
            <ResultBreakdown />
        </div>
    </section>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@500;700;800&display=swap');

* {
    font-family: 'Hanken Grotesk', sans-serif;
}

section {
    min-height: 100vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;

}

.container {
    width: 100%;
    height: 100%;
}

@media only screen and (min-width: 768px) {
    section {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .container {
        display: flex;
        align-items: center;
        width: 700px;
        height: 500px;
        background-color: white;
        border-radius: 40px;
        box-shadow: -15px -15px 15px white, 15px 15px 15px hsl(221, 100%, 96%);
    }
}
</style>