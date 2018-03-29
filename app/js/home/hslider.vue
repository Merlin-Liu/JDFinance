<template>
    <article class="">
        <slider :items="items" :cname="$style.slider"></slider>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{ name: item.href }">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>
<script type='text/ecmascript-6'>
    import Slider from '../core/slider.vue'

    export default {
        data () {
            return {
                items: [
                    {
                        href: 'home1',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t18724/53/552742550/28349/141d0cb1/5a976ab5N1f131e9c.jpg'
                    },
                    {
                        href: 'home2',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t18787/96/583735472/19041/545127d6/5a976b05N1a6a412a.jpg'
                    },
                    {
                        href: 'home3 ',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t15097/249/2268830415/20640/397e0ddf/5a976c28Nc5f227d1.jpg'
                    }
                ],
                enters: [
                    {
                        img: '//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png',
                        href: 'home',
                        title: '优惠券'
                    },
                    {
                        img: '//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
                        href: 'home',
                        title: '领红包'
                    },
                    {
                        img: '//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
                        href: 'home',
                        title: '抢钢镚'
                    },
                    {
                        img: '//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
                        href: 'home',
                        title: '白条提额'
                    },
                    {
                        img: '//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
                        href: 'home',
                        title: '优惠券'
                    }
                ]
            }
        },
        components: {
            Slider
        }
    }
</script>
<style lang='scss' module>
    @import "../../css/element.scss";
    .slider {
        margin-top: 120px;
        img {
            width: 100%;
        }
    }
    .list {
        @include list(row);
        background: #fff;
        padding-top: 40px;
        padding-bottom: 20px;
        justify-content: space-around;
        a {
            text-decoration: none;
        }
        .item {
            text-align: center;
            img {
                display: inline-block;
                width: 90px;
                height: 90px;
            }
            h4 {
                font-size: 26px;
                margin-top: 12px;
                color: #666;
            }
        }
    }
</style>