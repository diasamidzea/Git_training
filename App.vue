<template>

    <div style="display: inline">

        <h1>Ежедневник</h1>
        <p>Приготовьтесь</p>

        <input type="button" value="-" class="button1" v-on:click="quantityOfDiv--"/>
        <input type="button" value="+" class="button1" v-on:click="quantityOfDiv++"/>
        <div>
            <div class="div_vertiсal">
                <div v-for="i in quantityOfDiv" :key="i" class="div_horizontal">
                    <!--img src="./img/button-cross.gif" class="img_in_div"/-->
                </div>
            </div>

        </div>
    </div>

</template>

<script>
    export default {

//ветка 1
        
        data() {
            return {
                quantityOfDiv: 2
            }
        }
    }
</script>

<style scoped>


    p {
        font-size: 100%;
        text-shadow: 3px 3px 3px gray;
    }

    h1 {
        text-shadow: 3px 3px 3px gray;
    }

    .button1 {
        font-size: 40px;
        text-align: center;

        width: 50px;
        height: 50px;
    }

    .div_horizontal {
        display: inline-block;
        width: 100%;

        min-height: 100px;
        min-width: 100px;

        background-color: blue;
        border-color: black;
        border-style: solid;
        margin: 5px;
    }

    .div_vertiсal {
        margin: 10px;
        border-style: solid;

        display: inline-flex;

        width: 98%;
    }

    img_in_div {
        display: block;
        width: 100%;
    }

</style>