<template>
    <div class="home">
        <v-content class="transparent">
            <h1 class="t1">Hi, my name is </h1>
            <h2 class="t2">Ken Dong</h2>
            <v-spacer></v-spacer>
            <v-spacer></v-spacer>
            <h3 class="t3">A Software Problem-Solver</h3>
            <h4 class="t4"> I am an individual software developer based in Saskatoon, Saskatchewan, Canada.
                I am looking for a job now.</h4>
            <div class="b1">
                <v-btn>Get in Touch Now! </v-btn>
            </div>
        </v-content>
    </div>
</template>

<script>
    export default {
        name: "HomeComp"
    }
</script>

<style scoped>
    .home{
        margin: 1em 0;
    }
    .t1{
        font-family: "Apple SD Gothic Neo",serif;
        text-align: center;
        font-size: 28px;
        font-weight: lighter;
        line-height: 1.6;
    }
    .t2{
        font-family: "Avenir Next",serif;
        text-align: center;
        font-size: 60px;
        font-weight: revert;
        line-height: 2.3;
    }

    .t3{
        font-family: "Avenir Next",serif;
        text-align: center;
        font-size: 40px;
        font-weight: normal;
        line-height: 2.3;
    }

    .t4{
        font-family: "Avenir Next",serif;
        text-align: center;
        font-size: 25px;
        font-weight: normal;
        line-height: 2.3;
    }
    .b1{
        display: flex;
        justify-content: center;
        align-items: center;
        height: 200px;
        border: transparent;
    }

</style>
