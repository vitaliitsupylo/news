<template>
    <section class="banner_top_section">
        <div class="wrap_content">
            <div class="container">
                <div class="banner_main">
                    <p class="banner_text">
                        <span>ПЕРШЕ У СВІТІ</span> МОТОРНЕ МАСЛО З ПРИРОДНОГО ГАЗУ
                    </p>
                    <div class="banner_img">
                        <img src="/img/banner-main.png" alt="">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
    export default {
        name: 'topBanner'
    }

</script>

<style lang="scss">
      @import "../sass/index";

    .banner_top_section {
        width: 100%;
        position: relative;
        z-index: 5;
    }

    .banner_main {
        min-height: 235px;
        display: flex;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        .banner_text {
            font-weight: 700;
            font-size: 30px;
            line-height: 1;
            position: relative;
            z-index: 2;
            span {
                display: block;
                color: $colorRed;
                font-size: 90px;
                font-weight: 900;
            }
        }
        .banner_img {
            position: absolute;
            width: 400px;
            height: 200px;
            overflow: hidden;
            right: 0;
            bottom: 0;
            z-index: 1;
            img {
                position: relative;
                top: 0;
                left: 0;
                width: 100%;
                object-fit: cover;
            }
        }
    }
</style>