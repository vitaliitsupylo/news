<template>
    <article class="news_min">
        <a href="#" class="link_full_news"></a>
        <header class="news_header">
            <img class="news_img" src="/img/news1.png" alt="">
            <time class="news_time">01.12.2016</time>
        </header>
        <div class="news_content">
            <h1 class="news_title">В 2017 году в Ашхабаде состоится форум Энергетической Хартии</h1>
            <p class="news_text">01.12.2016 В 2017 году в Ашхабаде состоится очередная сессия
                конференции Энергетической Хартии, говори ....</p>
        </div>
        <a href="#" class="btn"><span>ПОДРОБНЕЕ</span><i class="icon-right-open"></i></a>
    </article>
</template>

<script>
    export default {
        name: "newsMin"
    }
</script>

<style lang="scss">
    @import "../sass/index";

    .news_min {
        width: 100%;
        position: relative;
        margin-bottom: 20px;
        display: flex;
        align-items: center;
        &:before {
            @include before_fig(100%, 3px, $colorGray);
            bottom: 0;
            left: 0;
        }
        .btn {
            position: absolute;
            bottom: 20px;
            right: 0;
            i {
                display: none;
            }
        }
        .link_full_news {
            position: absolute;
            z-index: 5;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: none;
        }
        .news_header {
            width: 100%;
            height: 262px;
            position: relative;
            margin-bottom: 20px;
            margin-right: 20px;
            overflow: hidden;
        }
        .news_content {
            margin-bottom: 20px;
            .news_title {
                font-size: 20px;
                font-weight: 700;
                margin-bottom: 5px;
            }
            .news_text {
                max-height: 80px;
                overflow: hidden;
            }
        }
    }

    .news_time {
        background-color: $colorBlueDark;
        color: #fff;
        padding: 20px 0;
        min-width: 180px;
        text-align: center;
        line-height: 0;
        font-weight: 700;
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: 2;
    }

    .news_img {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        z-index: 1;
        transition: transform $time, filter $time;
        transform: scale(1);
    }

    .chess {
        .news_min:nth-child(3n + 2),
        .news_min:nth-child(3n + 3) {
            display: flex;
            align-items: flex-start;
            flex-direction: row;
            flex: 1 1 35%;
            margin-right: 20px;
            padding-bottom: 0;
            &::before {
                width: 100%;
            }
            .link_full_news {
                display: block;
            }
            .news_header {
                height: 120px;
                margin-right: 15px;
                .news_time {
                    min-width: auto;
                    width: 100%;
                }
            }
            .news_content {
                .news_text {
                    display: none;
                }
                .news_title {
                    font-size: 17px;
                    overflow: hidden;
                    max-height: 82px;
                }
            }
            .btn {
                display: none;
            }
            &:hover {
                .news_header {
                    .news_img {
                        transform: scale(1.15);
                        filter: grayscale(100%);
                    }
                }
                .news_content {
                    .news_title {
                        text-decoration: underline;
                    }
                }
            }
        }
        .news_min:nth-child(3n+1) {
            flex-direction: column;
            .link_full_news {
                display: block;
            }
            .btn {
                display: none;
            }
            .news_header {
                margin-right: 0;
            }
            &::before {
                width: 72%;
            }
            &:hover {
                .news_header {
                    .news_img {
                        transform: scale(1.15);
                        filter: grayscale(100%);
                    }
                }
                .news_content {
                    .news_title {
                        text-decoration: underline;
                    }
                }
            }
        }
    }
</style>