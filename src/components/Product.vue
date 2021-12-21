<template>
    <div class="single_product">
        <img :src="productObject.thumb" alt="productObject.series">
        <h3>{{ productObject.series.toUpperCase() }}</h3>
    </div>
</template> 

<script>
export default {
    name: 'product',
    props: ['productObject']
}
</script>

<style lang="scss" scoped>
    .single_product{
        margin: 20px;
        width: calc(100% / 8);
        color: white;

        h3{
            margin-top: 10px;
            font-size: 12px;
        }
    }
</style>