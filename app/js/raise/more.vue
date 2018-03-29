<template>
    <panel title="更多福利" :class="$style.panel">
        <section :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t7456/56/1425209238/21928/f1fe492d/599cee57Naea99020.jpg?width=250&height=330" alt="">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t7894/126/1440046618/24763/5ce6a129/599cee04Ne77b3641.jpg?width=250&height=330" alt="">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t6385/103/1675552688/24265/91be4150/59549aedNa30670f7.jpg?width=250&height=330" alt="">
            <p>专项福利 > </p>
        </section>
    </panel>
</template>
<script type='text/ecmascript-6'>
    import Panel from '../core/panel.vue'
    export default {
        components: {
            Panel
        }
    }
</script>
<style lang="scss" module>
    @import "../../css/element";
    .panel {
        @include panel;
        .content {
            position: relative;
            @include flex(row);
            padding-bottom: 40px;
            justify-content: space-around;
            img {
                width: 33.333333%;
                height: 280px;
            }
            p {
                position: absolute;
                right: 20px;
                top: -112px;
                font-size: 28px;
                color: #999;
                height: 112px;
                line-height: 112px;
            }
        }
    }
</style>