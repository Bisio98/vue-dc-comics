<template>
    <body>
        <div class="container">CONTENT GOES HERE

            
        </div>
        <div class="big_buttons">
            <ul class="container">
                <li v-for="(element,index) in links" :key="index">
                    <img :src="require('@/assets/img/'+ element.ph)" alt="">
                    <span>{{ element.text }}</span>
                </li>
            </ul>
        </div>
    </body>
</template>

<script>
export default {
    name: 'Body',
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
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    body{
        background-color: #1C1C1C;

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

        .big_buttons{
            height: 200px;
            background-color:  #0C7CEC;
        }
    }
</style>