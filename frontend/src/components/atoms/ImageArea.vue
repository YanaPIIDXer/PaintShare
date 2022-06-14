<template>
    <div class="image-area">
        <image :src="image" />
    </div>
</template>

<script>
export default {
    name: 'ImageArea',
    props: {
        image: {
            type: String,
            default: '',
        },
    },
}
</script>

<style lang="scss" scoped>

</style>
