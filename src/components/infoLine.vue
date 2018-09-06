<template>
    <div class="inform_block">
        <div class="container">
            <div class="weather">
                <span class="city">Киев </span>
                <span class="temperature"></span>&#176;C
            </div>
            <div class="currency">
                КУРС ВАЛЮТ <i class="icon-dollar"></i><span class="dol"></span><i class="icon-euro"></i><span
                    class="euro"></span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'infoLine'
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