<template>
    <swiper :options="swiperOption">
        <!-- 
            <swiper :options="swiperOptionh">
                <swiper-slide>
                    <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021065/bale3_muny7s.jpg" title="Gareth Bale" description="Walish International" position="Winger"/>
                </swiper-slide>
                    <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021053/_106978677_hi053964919_jw7bif.jpg" title="Aaron Lennon" description="Ex English international" position="Winger"/>
                <swiper-slide>
                    <swiper :options="swiperOptionv">
                        <swiper-slide>
                            <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021042/1524836493_807927_noticia_normal_vm6jxf.jpg" title="Andres Iniesta" description="Ex Spainard and Barcelona maestro" position="Midfielder"/>
                        </swiper-slide>
                            <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021078/frank-lampard-and-four-other-footballers-who-have-had-literary-careers_tm1hlk.jpg" title="Frank Lampard" description="Ex England and Chelsea star" position="Midfielder"/>
                        <div class="swiper-pagination swiper-pagination-v" slot="pagination"></div>
                    </swiper>
                </swiper-slide>
                    <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021014/fbl-eng-pr-southampton-tottenham-5c9ce6bdeb32e5e548000001_hnifqq.jpg" title="Harry Kane" description="England and Tottenham forward" position="Striker"/>
                <div class="swiper-pagination swiper-pagination-h" slot="pagination"></div>
            </swiper>
        -->
        <!-- slides -->
        <swiper-slide>
        <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021078/frank-lampard-and-four-other-footballers-who-have-had-literary-careers_tm1hlk.jpg" title="Frank Lampard" description="Ex England and Chelsea star" position="Midfielder"/>
        </swiper-slide>
        <swiper-slide>
        <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021042/1524836493_807927_noticia_normal_vm6jxf.jpg" title="Andres Iniesta" description="Ex Spainard and Barcelona maestro" position="Midfielder"/>
        </swiper-slide>
        <swiper-slide>
        <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021014/fbl-eng-pr-southampton-tottenham-5c9ce6bdeb32e5e548000001_hnifqq.jpg" title="Harry Kane" description="England and Tottenham forward" position="Striker"/>
        </swiper-slide>
        <swiper-slide>
        <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590020987/https_3A_2F_2Fd1e00ek4.jpg" title="Lionel Messi" description="Greatest Of All time" position="Forward"/>
        </swiper-slide>
        <swiper-slide>
        <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021065/bale3_muny7s.jpg" title="Gareth Bale" description="Walish International" position="Winger"/>
        </swiper-slide>
        
        <swiper-slide>
        <Footballer image="https://res.cloudinary.com/dn89dampf/image/upload/v1590021053/_106978677_hi053964919_jw7bif.jpg" title="Aaron Lennon" description="Ex English international" position="Winger"/>
        </swiper-slide>     
        <div class="swiper-pagination" slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
</template>
<script>
import Footballer from './Footballer'
import 'swiper/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
    name: 'HomePage',
    components: {
        Footballer,
        swiper,
        swiperSlide
    },
    data() {
        return {

            swiperOption: {
              effect: 'coverflow',
              grabCursor: true,
              centeredSlides: true,
              slidesPerView: '2',
              loop: true,
              coverflowEffect: {
                rotate: 40,
                stretch: 0,
                depth: 100,
                modifier: 1,
                slideShadows : false
              },
              pagination: {
                el: '.swiper-pagination'
              }
            }

            
            /*
            swiperOption: {
              spaceBetween: 0,
              slidesPerView: 1.8,
              freeMode: true,
              loop: true,
              navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev'
              }
            }
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
             
            swiperOption: {
                direction : 'vertical',
                pagination: {
                    el: '.swiper-pagination',
                    type: 'bullets'
                },
            }
            //nested swips
            swiperOptionh: {
                spaceBetween: 18,
                pagination: {
                el: '.swiper-pagination-h',
                clickable: true
                }
            },
            swiperOptionv: {
                direction: 'vertical',
                spaceBetween: 18,
                pagination: {
                el: '.swiper-pagination-v',
                clickable: true
                }
            },
                
            */
           
                 
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
      width : 90%;
    }
    
</style>