<template>
    <swiper :options="swiperOption">
        <!-- 
            nested slider
        <swiper :options="swiperOptionh">
            <swiper-slide>
                <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
            </swiper-slide>
                <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
            <swiper-slide>
                <swiper :options="swiperOptionv">
                    <swiper-slide>
                        <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
                    </swiper-slide>
                        <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
                    <div class="swiper-pagination swiper-pagination-v" slot="pagination"></div>
                </swiper>
            </swiper-slide>
                <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
            <div class="swiper-pagination swiper-pagination-h" slot="pagination"></div>
        </swiper>
        -->
        <!-- slides -->
        <swiper-slide>
        <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--4NgMf3RF--/v1521804358/avengers.jpg" title="Avengers : Infinity War" description="Thanos is around" duration="2hrs"/>
        </swiper-slide>
        <swiper-slide>
        <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
        </swiper-slide>
        <!-- more movies --> 
        <swiper-slide>
        <Movie image="http://res.cloudinary.com/og-tech/image/upload/s--qXaW5V3E--/v1521804426/wakanda.jpg" title="Black Panther" description="Wakanda Forever" duration="2hrs15mins"/>
        </swiper-slide>

        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
</template>
<script>
import Movie from './Movie'
import 'swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
    name: 'HomePage',
    components: {
        Movie,
        swiper,
        swiperSlide
    },
    data() {
        return {
            /*
            swiperOption: {
                direction : 'vertical',
                pagination: {
                    el: '.swiper-pagination',
                    type: 'bullets'
                },
            }
            //nested swips
            swiperOptionh: {
                spaceBetween: 50,
                pagination: {
                el: '.swiper-pagination-h',
                clickable: true
                }
            },
            swiperOptionv: {
                direction: 'vertical',
                spaceBetween: 50,
                pagination: {
                el: '.swiper-pagination-v',
                clickable: true
                }
            },
            swiperOptions : {
                slidesPerView: 5,
                spaceBetween: 0,
                freeMode: true,
                loop: true,
                navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev'
                }
            }
            */
           swiperOption: {
              effect: 'coverflow',
              grabCursor: true,
              centeredSlides: true,
              slidesPerView: '5',
              coverflowEffect: {
                rotate: 50,
                stretch: 0,
                depth: 100,
                modifier: 1,
                slideShadows : false
              },
              pagination: {
                el: '.swiper-pagination'
              }
            }
            
        }
    }
}
</script>

<style scoped>
    .swiper-slide{
      display: flex;
      justify-content: center;
      flex-direction: column;
    }
    .swiper-container {
      height : 500px;
    }
</style>