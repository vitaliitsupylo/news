<template>
    <div>
        <topBanner/>
        <infoLine/>
    </div>
</template>

<script>
    import topBanner from '../components/topBanner';
    import infoLine from '../components/infoLine';

    export default {
        name: 'home',
        components: {
            topBanner, infoLine
        }
    }

</script>

<style lang="scss">

</style>