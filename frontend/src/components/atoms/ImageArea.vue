<template>
    <div class="image-area">
        <img :src="image" />
    </div>
</template>

<script>
export default {
    name: 'ImageArea',
    props: {
        image: {
            type: String,
            default: '',
            require: false,
        },
    },
}
</script>

<style lang="scss" scoped>

</style>
