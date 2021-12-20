<template>
    <footer>
        
            <div class="top">
                <div class="container">
                    <div class="links">
                        <div>
                            <ul>
                                <li class="name_col">DC COMICS</li>
                                <li v-for="(element,index) in dcComics" :key="index">{{ element }}</li>
                            </ul>
                            <ul>
                                <li class="name_col">SHOP</li>
                                <li v-for="(element,index) in shop" :key="index">{{ element }}</li>
                            </ul>
                            
                        
                        </div>
                        <ul>
                            <li class="name_col">DC</li>
                            <li v-for="(element,index) in dc" :key="index">{{ element }}</li>
                        </ul>
                        <ul>
                            <li class="name_col">SITES</li>
                            <li v-for="(element,index) in sites" :key="index">{{ element }}</li>
                        </ul>
                    </div>
                    <div class="logo_bot"> 
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </div>
                    
                </div>
                
            </div>

            <div class="bottom">
                <div class="container">
                    <div>
                        <button>SIGN-UP NOW!</button>
                    </div>
                    <ul class="socials">
                        <li>FOLLOW US</li>
                        <li><img src="../assets/img/footer-facebook.png" alt="Facebook logo"></li>
                        <li><img src="../assets/img/footer-twitter.png" alt="Twitter logo"></li>
                        <li><img src="../assets/img/footer-youtube.png" alt="Youtube logo"></li>
                        <li><img src="../assets/img/footer-pinterest.png" alt="Pinterest logo"></li>
                        <li><img src="../assets/img/footer-periscope.png" alt="Periscope logo"></li>
                    </ul>
                </div>
            </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data: function(){
        return{
            dcComics:[
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News'
            ],
            shop:[
                'Shop DC',
                'Shop DC Collectibles'
            ],
            dc: [
                'Terms Of Use',
                'Provacy Policy(New)',
                'Ad Choices',
                'Advertising',
                'Jobs',
                'Subscriptions',
                'Talent Workshops',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact us'
            ],
            sites: [
                'DC',
                'MAD Magazine',
                'DC Kids',
                'DC Universe',
                'DC Power Visa'
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    footer{
       background-color: #303030;
    }

    ul{
        list-style: none;
    }

    .top{
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        display: flex;

        .container{
        position: relative;
        height: 400px;
        display: flex;
        justify-content: space-between;
        overflow: hidden;
        }

        .links{
        display: flex;
        margin-top: 20px;
        color: gray;
        line-height: 20px;
        }

        .logo_bot img{
        position: relative;
        bottom: 50px;

        img{
            height: 400px;
            width: auto;
        }
        }

        .name_col{
        font-size: 22px;
        line-height: 30px;
        color: white;
        font-weight: 800;
        }

        ul {
        margin-right: 20px;
        }
    }



    .bottom{
        .container{
        display: flex;
        overflow: hidden;
        justify-content: space-between;
        height: 150px;
        align-items: center;
        position: relative;
        z-index: 2;
        }

        button{
        padding: 15px;
        color: white;
        font-weight: 700;
        background-color:  #303030;
        border: 2px solid #0C7CEC;
        }

        ul{
        display: flex;
        align-items: center;
        }

        li{
        margin: 0 10px;
        color: #0C7CEC ;
        font-size: 25px;
        font-weight: 700;
        }

    }
</style>