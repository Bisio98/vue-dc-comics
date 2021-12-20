<template>
    <header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="DC Logo">
            <ul>
                <li v-for="(element,index) in pages" :key="index"> {{ element.singlePage }}</li>
            </ul>
        </div>
        
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function() {
        return{
            pages: [ {
                singlePage: 'CHARACTERS',
                activeItem: false
            },
            {
                singlePage: 'COMICS',
                activeItem: true
            },
            {
                singlePage: 'MOVIES',
                activeItem: false
            },
            {
                singlePage: 'TV',
                activeItem: false
            },
            {
                singlePage: 'GAMES',
                activeItem: false
            },
            {
                singlePage: 'COLLECTIBLES',
                activeItem: false
            },
            {
                singlePage: 'VIDEOS',
                activeItem: false
            },
            {
                singlePage: 'FANS',
                activeItem: false
            },
            {
                singlePage: 'NEWS',
                activeItem: false
            },
            {
                singlePage: 'SHOP',
                activeItem: false
            }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    header{
        background-color: white;
        .container{
            display: flex;
            justify-content: space-between ;
            line-height: 100px;
            align-items: center;
            height: 130px;
        }

        img{
            height: 70px;
            width: 70px;
        }
            ul{
        list-style: none;
        display: flex;
        }

        li{
            margin: 0px 10px;
            font-weight: 00;
        }

        .active{
            border-bottom: 3px solid #0C7CEC;
        }
    }
</style>