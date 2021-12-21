<template>
    <body>
        <section class="background_img">
        </section>

        <section class="current_series">
            <div class="container">
                <h2>CURRENT SERIES</h2>
            </div>

            <div class="container">
                <div class="comics">
                    <product class="single_comic" v-for="(comic,index) in current_comics" :key="index" :productObject="comic"/> 
                </div>
            </div>

            <div class="others">
                <button>LOAD MORE</button>
            </div>
        </section>

        <section class="big_buttons">
            <ul class="container">
                <li v-for="(element,index) in links" :key="index">
                    <img :src="require('@/assets/img/'+ element.ph)" alt="">
                    <span>{{ element.text }}</span>
                </li>
            </ul>
        </section>
    </body>
</template>

<script>
import Product from './Product.vue'

export default {
    name: 'Body',
    components: {
        Product
    },
    data: function(){
        return{
            links: [{
                ph: 'buy-comics-digital-comics.png',
                text: 'DIGITAL COMICS'
            },
            {
                ph: 'buy-comics-merchandise.png',
                text: 'DC MERCHANDISE'
            },
            {
                ph: 'buy-comics-subscriptions.png',
                text: 'SUBSCRIPTION'
            },
            {
                ph: 'buy-comics-shop-locator.png',
                text: 'COMIC SHOP LOCATOR'
            },
            {
                ph: 'buy-dc-power-visa.svg',
                text: 'DC POWER VISA'
            },
            ],
            current_comics:[
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book"
                },
                {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/general.scss';

    body{
        background-color: #1C1C1C;

        .background_img{
            background-image: url('../assets/img/jumbotron.jpg');
            height: 450px;
            background-size: cover;
        }

        .current_series{
            
            h2{
                position: relative;
                bottom: 30px;
                color: white;
                display: inline-block;
                padding: 20px;
                background-color: #0C7CEC;
            }

            .comics{
                display: flex;
                flex-wrap: wrap;
                justify-content: space-around;
            }

            .others{
                text-align: center;
                button{
                    padding: 15px;
                    background-color: #0C7CEC;
                    border: 2px solid #0C7CEC;
                    margin: 10px;
                    color: white;
                }
            }
        }

        .big_buttons{
            height: 200px;
            background-color:  #0C7CEC;

            ul{
                height: 200px;
                list-style: none;
                color: white;
                display: flex;
                justify-content: space-evenly;
                align-items: center;

                li{
                    display: flex;
                    align-items: center;
                }

                img{
                    height: 60px;
                    width: auto;
                    margin: 5px;
                }
            }
        
            div{
            text-align: center;
            color: rgb(36, 23, 23);
            height: 200px;
            }
        }
    }
</style>