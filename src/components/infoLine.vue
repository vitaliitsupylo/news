<template>
    <div class="inform_block">
        <div class="container">
            <div class="weather">
                <span class="city">Киев </span>
                <span class="temperature">{{ temperature }}</span>&#176;C
            </div>
            <div class="currency">
                КУРС ВАЛЮТ <i class="icon-dollar"></i><span class="dol">{{currencyUSD}}</span><i
                    class="icon-euro"></i><span
                    class="euro">{{currencyEUR}}</span>
            </div>
        </div>
    </div>
</template>

<script>
    const axios = require('axios');

    function getValue(arr, str) {
        for (let i = 0; i < arr.length; i++) {
            if (arr[i]['ccy'].toUpperCase() === str.toUpperCase()) {
                return arr[i]['sale'].slice(0, 5);
            }
        }
    }

    export default {
        name: 'infoLine',
        data() {
            return {
                temperature: this.getTemperature(),
                currencyUSD: '00',
                currencyEUR: '00',
                currency: this.getCurrency()
            }
        },
        methods: {
            getTemperature() {
                axios({
                    method: 'get',
                    url: 'http://api.openweathermap.org/data/2.5/weather?lat=50.4546600&lon=30.5238000&APPID=eb8183acf2cb85c1351fe1826283fc36'
                })
                    .then((res) => {
                        let tempData = Math.round(res.data.main.temp - 273);
                        this.temperature = (tempData > 0) ? `+ ${tempData}` : tempData;
                    }, () => {
                        this.temperature = ' no Internet';
                    });
            },
            getCurrency() {
                axios({
                    method: 'get',
                    url: 'https://api.privatbank.ua/p24api/pubinfo?json&exchange&coursid=5'
                })
                    .then((res) => {
                        this.currencyUSD = getValue(res.data, 'USD');
                        this.currencyEUR = getValue(res.data, 'EUR');
                    }, () => {
                        this.currencyUSD = '00';
                        this.currencyEUR = '00';
                    });
            }
        }
    }
</script>

<style lang="scss">
    @import "../sass/index";

    .inform_block {
        width: 100%;
        position: relative;
        z-index: 5;
        background-color: #241e1e;
        .container {
            display: flex;
            min-height: 60px;
            -webkit-box-pack: justify;
            -ms-flex-pack: justify;
            justify-content: space-between;
            -webkit-box-align: center;
            -ms-flex-align: center;
            align-items: center;
        }
    }

    .weather {
        color: #fff;
    }

    .currency {
        color: #fff;
        padding-right: 9px;
        text-transform: uppercase;
        i {
            margin-left: 25px;
            font-size: 27px;
            color: $colorRed;
            position: relative;
            top: 3px;
        }
    }
</style>