<template>
    <footer class="footer_main">
        <div class="footer_bg">
            <span></span>
            <img src="/img/bg-footer.png" alt="">
        </div>
        <div class="container">
            <div class="footer_nav">
                <a href="#">ПРАВИЛА ПОЛЬЗОВАНИ</a>
                <a href="#">РЕКЛАМА</a>
                <a href="#">КОНАКТЫ</a>
            </div>
            <p>
                Использование любых материалов, размещенных на сайте, разрешается при условии ссылки на Forbes.net.ua. Для
                интернет-изданий обязательна прямая, открытая для поисковых систем гиперссылка. Ссылка должна быть размещена
                вне зависимости от полного либо частичного использования матириалов. Гиперссылка (для интернет-изданий) -
                должна быть размещена в подзаголовке или в первом абзаце материала. Перепечатка, копирование,
                воспроизведение или иное использование материалов, в которых содержится ссылка на агенства
                Інтерфакс-Україна, Українські Новини, УНІАН, Комсомольскую правду в Украине, а также Reuters и Associated
                Press, строго запрещены. Категорически запрещено перепечатывать материалы, опубликованные в рамках
                партнерства с Русской Службой Би-би-си и Украинской службой Би-би-си. Материалы, отмеченные знаком
                “Реклама”, публикуются на правах рекламы.
            </p>
            <p class="copyright">
                <span>&#169;2017 “ОИЛ ГАЗ ЕНЕРДЖИ”</span>
                <b>&#169;2017 OIL GAZ ENERDGYтм</b> as to materials published on oil-gaz-energy.com.ua
                All Rights Reserved Торговая марка OIL-GAZ-Energy является исключительной собственностью OIL-Gaz-Energy inc.
                и
                используется в соотвествии с лицензионным договором с Oil-Gaz-Energy inc.
            </p>
        </div>
    </footer>
</template>

<script>

</script>

<style lang="scss">
    @import "../sass/index";

    .footer_main {
        position: relative;
        z-index: 5;
        .container {
            position: relative;
            z-index: 5;
            padding-top: 80px;
            color: #f5f5f5;
            padding-bottom: 135px;
            p {
                margin-bottom: 40px;
            }
        }
        .copyright {
            b, span {
                text-transform: uppercase;
                font-weight: 400;
            }
            span {
                display: block;
            }
        }
    }

    .footer_bg {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 100%;
        height: 100%;
        span {
            position: absolute;
            top: 0;
            width: 100%;
            height: 100%;
            left: 0;
            background: linear-gradient(to top, #143666 0%, #13386c 100%);
            display: block;
            z-index: 2;
            opacity: .9;
        }
        img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            -o-object-fit: cover;
            object-fit: cover;
            z-index: 1;
        }
    }

    .footer_nav {
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -webkit-box-align: start;
        -ms-flex-align: start;
        align-items: flex-start;
        -webkit-box-pack: start;
        -ms-flex-pack: start;
        justify-content: flex-start;
        margin-bottom: 50px;
        a {
            text-transform: uppercase;
            display: inline-block;
            color: #fff;
            &:hover {
                text-decoration: underline;
            }
        }
    }


</style>