<template>
    <main class="wrap_list_news">
        <div class="control_list">
            <h2 class="title_block">НОВОЕ НА САЙТЕ</h2>
            <div class="control_wrap">
                <div class="chess_btn active">
                    <i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i>
                </div>
                <div class="list_btn">
                    <i></i><i></i><i></i><i></i><i></i><i></i>
                </div>
            </div>
        </div>
        <div class="list_news">
            <newsMin/>
        </div>
        <div class="moving_news">
            <a href="#" class="moving_before">
                <span><i class="icon-left-open"></i>Предыдущая страница</span>
            </a>
            <a href="#" class="moving_after">
                <span>Следующая страница <i class="icon-right-open"></i></span>
            </a>
        </div>
        <ul class="bread_crumbs">
            <li><a href="#">Новость</a></li>
            <li><a href="#">Еще новость</a></li>
            <li>И еще новость</li>
        </ul>
        <a href="#" class="banner_line">
            <img src="/img/banner_line.png" alt="">
        </a>
    </main>
</template>

<script>
    import newsMin from '../components/newsMin';

    export default {
        name: 'main',
        components: {
            newsMin
        }
    }
</script>

<style lang="scss">
    @import "../sass/index";

    .wrap_list_news {
        width: 100%;
        max-width: 850px;
    }

    .control_list {
        height: 85px;
        width: 100%;
        align-items: center;
        display: flex;
        justify-content: space-between;
        border-bottom: 3px solid #dddddd;
    }

    .control_wrap {
        display: flex;
        align-self: center;
    }

    .chess_btn {
        width: 50px;
        height: 50px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        padding: 10px 10px 8px;
        cursor: pointer;
        transition: $time;
        background-color: #e5e2e2;
        i {
            width: 8px;
            height: 8px;
            display: block;
            transition: $time;
            margin-bottom: 2px;
            background-color: #241e1e;
        }
        &.active,
        &:hover {
            background-color: #241e1e;
            i {
                background-color: #e5e2e2;
            }
        }
    }

    .list_btn {
        width: 50px;
        height: 50px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        padding: 10px 10px 8px;
        cursor: pointer;
        transition: $time;
        background-color: #e5e2e2;
        margin-left: 18px;
        i {
            width: 8px;
            transition: $time;
            height: 8px;
            display: block;
            margin-bottom: 2px;
            background-color: #241e1e;

            &:nth-child(even) {
                width: 20px;
            }
        }
        &.active,
        &:hover {
            background-color: #241e1e;
            i {
                background-color: #e5e2e2;
            }
        }
    }
    .list_news {
        padding-top: 25px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
</style>