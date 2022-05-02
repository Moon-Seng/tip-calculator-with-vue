<template>

<div class="container">

    <div class="logo">
        <img src="./assets/logo.svg" alt="">
    </div>

    <div class="main-card">
        <div class="col-12 col-lg-6 left-content">
            <div class="bill">
                <label class="form-label" for="bill">Bill</label>
                <input class="form-control" type="text" name="" id="bill" placeholder="0.00">
            </div>

            <div class="selectTip">
                <label class="form-label" for="">Select Tip %</label>

                <div class="tips">
                    <button class="tipBtn base-button-tip">5%</button>
                    <button class="tipBtn base-button-tip">10%</button>
                    <button class="tipBtn base-button-tip">15%</button>
                    <button class="tipBtn base-button-tip">25%</button>
                    <button class="tipBtn base-button-tip">50%</button>
                    <input type="text" placeholder="Custom">
                </div>
            </div>

            <div class="numberOfPeople">
                <label class="form-label" for="numPeople">Number Of People <span>Can't be zero</span></label>
                <input class="form-control" type="text" name="" placeholder="0" id="">
            </div>

        </div>

        

        <div class="col-12 col-lg-6 right-content">

            <div class="right-card">
                <div class="result">
                    <div class="tip-amount">
                        <div class="tip-amount-text">
                            <h6>Tip Amount</h6>
                            <p>/ person</p>
                        </div>

                        <div class="tip-amount-number">
                            <h1>$0.00</h1>
                        </div>
                    </div>

                    <div class="total">
                        <div class="total-text">
                            <h6>Total</h6>
                            <p>/ person</p>
                        </div>

                        <div class="total-number">
                            <h1>$0.00</h1>
                        </div>
                    </div>
                </div>

                <div class="reset">
                    <button>Reset</button>
                </div>
            </div>

        </div>
    </div>
</div>

</template>

<script>
export default {
    data(){
        return{
            
        }
    },
    methods:{

    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap');

*{
    padding: 0;
    margin: 0;
    box-sizing: border-box !important;
    font-family: 'Space Mono', monospace;
    font-size: 24px;
}

body{
    background-color: hsl(185, 41%, 84%) !important;
}

/* Base */
.base-button-tip{
    border: none;
    padding: .5rem 2rem;
    border-radius: 6px;
    color: white;
    background-color: hsl(183, 100%, 15%);
    margin: .5rem .8rem .5rem 0;
    font-weight: bold;
    min-width: 140px;
}

label{
    color: hsl(186, 14%, 43%);
    font-weight: bold;
}

/* End Base */

.container{
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    justify-content: center;
}

.logo{
    margin-bottom: 2rem;
}

.main-card{
    border-radius: 1rem;
    overflow: hidden;
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    width: 1065px;
}

.left-content {
    padding: 3rem;
}

.bill{
    margin-bottom: 1.5rem;
}


.bill input{
    background-image: url("./assets/icon-dollar.svg");
    background-repeat: no-repeat;
    background-position-x: 20px;
    background-position-y: 50%;
    text-align: right;
    background-color: hsl(189, 41%, 97%);
    font-weight: bold;
    border: none;
    cursor: pointer;
}

.bill input:focus{
    border: 2px solid hsl(172, 67%, 45%);
    background-color: hsl(189, 41%, 97%);
    box-shadow: none;
}

.selectTip{
    margin-bottom: 1.5rem;
}

.tips{
    display: flex;
    flex-wrap: wrap;
}

.tips input{
    width: 140px;
    height: 60px;
    border: none;
    margin: .5rem .8rem .5rem 0;
    text-align: center;
    background-color: hsl(189, 41%, 97%);
    border-radius: 8px;
    cursor: pointer;
}

.tips input:active{
    border: none;
}

.tips input:focus{
    border: 2px solid hsl(172, 67%, 45%);
    background-color: hsl(189, 41%, 97%);
    box-shadow: none;
}

.numberOfPeople label{
    width: 100%;
}

.numberOfPeople span{
    color: rgb(238, 52, 52);
    margin-top: 10px;
    font-size: 18px;
    float: right;
}

.numberOfPeople input{
    cursor: pointer;
    background-image: url("./assets/icon-person.svg");
    background-repeat: no-repeat;
    background-position-x: 20px;
    background-position-y: 50%;
    text-align: right;
    background-color: hsl(189, 41%, 97%);
    font-weight: bold;
    border: none;
}

.numberOfPeople input:focus{
    border: 2px solid hsl(172, 67%, 45%);
    background-color: hsl(189, 41%, 97%);
    box-shadow: none;
}

.right-card{
    padding: 2rem;
    background-color: hsl( 183, 100%, 15%);
    margin: 1rem;
    height: 90%;
    border-radius: 1rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.tip-amount , .total{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.result{
    margin-top: 2rem;
}

.tip-amount{
    margin-bottom: 1.5rem;
}

.tip-amount-text h6 , .total h6{
    color: white;
    margin-bottom: 0;
    font-weight: bold;
}

.tip-amount-text p , .total p{
    color: rgba(255, 255, 255, 0.7);
    font-size: 18px;
}

.tip-amount-number h1 , .total-number h1{
    color: hsl(172, 67%, 45%);
    font-weight: bold;
}

.reset button{
    text-transform: uppercase;
    font-weight: bold;
    width: 100%;
    padding: .5rem 0;
    background-color: hsl(172, 67%, 45%);
    border: none;
}

.reset button:hover{
    background-color: hsl(185, 79%, 71%);

}

@media screen and (max-width : 1070px) {

    #app{
        margin: 4rem auto;
    }

    .container{
        height: fit-content;
        padding: 5rem auto;
    }

    .main-card{
        width: 700px;
        height: fit-content ;
    }
}

@media screen and (min-width: 1600px) {
    .main-card{
        width: 1300px;
    }

    .logo{
        margin-bottom: 6rem;
    }
}

@media screen and (max-width: 500px) {
    *{
        font-size: 16px;
    }

    .main-card{
        width: 98%;
    }

    .left-content{
        padding: 1rem;
    }

    .base-button-tip , .tips input{
        height: 50px;
    }

    .numberOfPeople span{
        font-size: 12px;
    }
}


@media screen and (max-width : 1300px) {
    .main-card{
        width: 99%;
    }
}


</style>
