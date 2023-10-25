<template>
    <h1>This is the index.vue page</h1>
</template>

<script>
export default {
    async setup() {
        const { data: productResponse } = await useFetch('https://dummyjson.com/products/1')

        console.log('productResponse', productResponse)

        useHead({
            title: 'Hello there'
        })

        return { hello: 'there' }
    }
}
</script>
