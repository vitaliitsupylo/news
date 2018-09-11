<template>
    <div>
        <topBanner/>
        <infoLine/>
        <div class="wrap_main_content">
            <div class="wrap_content">
                <div class="container">
                    <mainBlock/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import topBanner from '../components/topBanner';
    import infoLine from '../components/infoLine';
    import mainBlock from '../components/main';

    export default {
        name: 'home',
        components: {
            topBanner,
            infoLine,
            mainBlock
        }
    }

</script>

<style lang="scss">

</style>