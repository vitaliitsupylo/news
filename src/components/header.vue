<template>
    <header class="header_main">
        <div class="container">
            <div class="header_left">
                <div class="btn_menu">
                    <i></i>
                    <i></i>
                    <i></i>
                </div>
                <a href="#" class="logo">
                    <span>ENERGY</span>
                    НЕФТЬ & ГАЗ
                </a>
            </div>
            <nav class="nav_main">
                <a href="#" class="active"><span>Н</span>ОВОСТИ</a>
                <a href="#"><span>Р</span>ЕДАКЦИЯ</a>
                <a href="#"><span>Ж</span>УРНАЛ</a>
                <a href="#"><span>Ф</span>ОТОГАЛЕРЕЯ</a>
            </nav>
            <div class="social_set">
                <a href="#"><i class="icon-facebook"></i></a>
                <a href="#"><i class="icon-twitter"></i></a>
                <button class="open_search"><i class="icon-search"></i></button>
            </div>
            <!-- BEGIN MENU -->
            <div class="menu">
                <div class="close_menu"><i class="icon-cancel"></i></div>
                <ul class="nav_category_list">
                    <li><a href="#">НОВОСТИ</a></li>
                    <li><a href="#">РЕДАКЦИЯ</a></li>
                    <li><a href="#">ЖУРНАЛ</a></li>
                    <li><a href="#">UNCONVENTIONAL GAS</a></li>
                    <li><a href="#">RENEWABLE ENERGY</a></li>
                    <li><a href="#">ЭНЕРГОЭФФЕКТИВНОСТЬ</a></li>
                    <li><a href="#">СОБЫТИЯ</a></li>
                </ul>
                <ul class="nav_info_list">
                    <li><a href="#">ПРАВИЛА ПОЛЬЗОВАНИЯ</a></li>
                    <li><a href="#">РЕКЛАМА</a></li>
                    <li><a href="#">КОНТАКТЫ</a></li>
                </ul>
                <div class="social_menu">
                    <a href=""><i class="icon-facebook"></i>FACEBOOK</a>
                    <a href=""><i class="icon-twitter"></i>TWITTER</a>
                </div>
            </div>
            <!-- END MENU -->
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        }
    }
</script>

<style lang="scss">
    @import "../sass/index";

    .header_main {
        width: 100%;
        background: linear-gradient(to top, #143666 0%, #13386c 100%);
        position: absolute;
        top: 0;
        left: 0;
        z-index: 10;
        .container {
            display: flex;
            -webkit-box-pack: justify;
            -ms-flex-pack: justify;
            justify-content: space-between;
            -webkit-box-align: center;
            -ms-flex-align: center;
            align-items: center;
            height: 100px;
            position: relative;
        }
        &.active {
            position: fixed;
            top: -300px;
            opacity: 0;
            .container {
                height: 70px;
            }
            &.top_head {
                -webkit-transition: top .5s;
                transition: top .5s;
                top: 0;
                opacity: 1;
            }
        }
    }

    .logo {
        display: block;
        width: 105px;
        font-size: 16px;
        color: #fff;
        font-weight: 700;
        text-transform: uppercase;
        text-align: center;
        line-height: 1;
        span {
            display: block;
            font-size: 27px;
        }
    }

    .header_left {
        display: flex;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
    }

    .btn_menu {
        width: 44px;
        height: 38px;
        background-color: #fff;
        position: relative;
        margin-right: 45px;
        cursor: pointer;
        transition: background-color .3s;
        i {
            display: block;
            height: 4px;
            width: 30px;
            position: absolute;
            left: 7px;
            transition: background-color .3s;
            background-color: $colorBlue;
            &:first-child {
                top: 8px;
            }
            &:nth-child(2) {
                top: 17px;
            }
            &:last-child {
                bottom: 8px;
            }
        }
        &:hover {
            background-color: #202530;
            i {
                background-color: #fff;
            }
        }
    }

    .nav_main {
        width: 100%;
        max-width: 565px;
        display: flex;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
        a {
            font-size: 16px;
            color: #fff;
            text-transform: uppercase;
            margin: 0 5px;
            position: relative;
            span {
                transition: color .3s;
            }
            &::before {
                @include before_fig(0, 1px, $colorRed);
                bottom: 0;
                left: 0;
                -webkit-transition: .3s;
                transition: .3s;
            }
            &:hover, &.active {
                &:before {
                    width: 100%;
                }
                span {
                    color: $colorRed;
                }
            }
        }
    }

    .menu {
        position: absolute;
        top: -1000px;
        left: 0;
        background-color: rgba(20, 54, 105, .98);
        width: 100%;
        height: 480px;
        z-index: 50;
        display: flex;
        opacity: 0;
        transition: opacity .5s, top .4s;
        align-items: flex-start;
        padding-left: 130px;
        .close_menu {
            position: absolute;
            left: 0;
            height: 100%;
            width: 80px;
            display: flex;
            cursor: pointer;
            color: #fff;
            transition: color .3s;
            background-color: $colorBlue;
            &:hover {
                color: $colorRed;
            }
            i {
                margin: auto;
                font-style: normal;
                font-size: 40px;
                font-weight: 700;
                position: relative;
            }
        }
        .nav_category_list, .nav_info_list {
            margin-right: 10%;
            margin-top: 15%;
            li {
                a {
                    color: rgba(255, 255, 255, .8);
                    font-size: 20px;
                    text-transform: uppercase;
                    margin: 10px 0;
                    position: relative;
                    -webkit-transition: color;
                    transition: color;
                    line-height: 1;
                    display: inline-block;
                    &::before {
                        @include before_fig(6px, 6px, $colorRed);
                        left: -12px;
                        top: 6px;
                        border-radius: 50%;
                        opacity: 0;
                        display: block;
                        transition: opacity .3s;
                    }
                    &:hover {
                        color: rgba(255, 255, 255, 1);
                        &::before {
                            opacity: 1;
                        }
                    }
                }
            }
        }
    }

    .menu.active {
        top: 0;
        opacity: 1;
    }

    .social_menu {
        margin-top: 15%;
        display: flex;
        width: 100%;
        max-width: 260px;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        a {
            display: block;
            color: #fff;
            font-size: 20px;
            text-transform: uppercase;
            border: solid 1px #fff;
            height: 50px;
            padding-left: 23%;
            margin-bottom: 19px;
            line-height: 52px;
            transition: color .3s;
            &:hover {
                color: $colorRed;
            }
            i {
                margin-right: 20px;
            }
        }
    }

    .social_set {
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        a, .open_search {
            color: #fff;
            height: 38px;
            font-size: 25px;
            text-align: center;
            display: block;
            line-height: 35px;
            width: 46px;
            background-color: transparent;
            cursor: pointer;
            transition: color .3s;
            border-right: solid 1px rgba(204, 204, 204, .16);
            border-bottom: solid 1px rgba(204, 204, 204, 0);
            i {
                font-style: normal;
            }
            &:first-child {
                border-left: solid 1px rgba(204, 204, 204, .16);
            }
            &:hover {
                border-bottom: solid 1px rgba(204, 204, 204, .16);
                color: #241e1e;
            }
        }
    }

    .open_search {
        border-top: none;
        border-left: none;
        i {
            position: relative;
            top: -2px;
        }
    }

</style>
