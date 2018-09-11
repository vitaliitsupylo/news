<template>
    <main>
        <Header/>

        <router-view></router-view>


        <Footer/>
    </main>
</template>

<script>
    import Header from '@/components/header.vue'
    import Footer from '@/components/footer.vue'

    export default {
        name: 'home',
        components: {
            Header,
            Footer
        }
    }
</script>

<style lang="scss">

    @import "sass/reset";
    @import "sass/index";
    @import "sass/fonst";

    body {
        font: 400 17px/1.64 $proxima;
        color: #202530;
        padding-top: 100px;
        position: relative;
        min-width: 315px;
    }

    .container {
        width: 100%;
        max-width: 1170px;
        margin: auto;
        padding: 0 10px;
    }

    .bunner_bg {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        right: 0;
        z-index: 1;
        bottom: 0;
        img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    .wrap_content {
        width: 100%;
        max-width: 1365px;
        background-color: #fff;
        margin: auto;
        position: relative;
        z-index: 2;
    }

    .btn {
        display: inline-block;
        height: 50px;
        line-height: 50px;
        color: #fff;
        font-weight: 700;
        background: $colorSkyGrad;
        border: solid 2px transparent;
        padding: 0 38px;
        z-index: 5;
        -webkit-transition: .3s;
        transition: .3s;
        &:hover {
            background: #fff;
            color: #000;
            border: solid 2px #000;
        }
    }

    .title_block {
        color: #000;
        font-size: 25px;
        text-transform: uppercase;
        position: relative;
        font-weight: 700;
    }

    .wrap_main_content {
        .container {
            display: flex;
            justify-content: space-between;
        }
        .wrap_content {
            padding-bottom: 60px;
        }
    }

    .bread_crumbs {
        display: flex;
        margin: 15px 0;
        li, a {
            text-transform: uppercase;
        }
        li {
            margin-right: 10px;
            position: relative;
            transition: .3s;
            &::after {
                content: "/";
                top: 0;
                position: relative;
                right: -5px;
                font-size: 22px;
            }
            &:hover {
                color: $colorRed;
            }
            &:last-child {
                font-weight: 700;
                color: $colorRed;
                &::after {
                    color: transparent;
                }
            }
        }
    }

    .banner_line {
        width: 100%;
        height: 130px;
        display: block;
        position: relative;
        margin-bottom: 20px;
        img, video {
            position: absolute;
            width: 100%;
            height: 100%;
            object-fit: cover;
            top: 0;
            left: 0;
        }
    }

</style>
