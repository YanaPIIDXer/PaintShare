<template>
    <div class="image-area">
        <img v-if="image" :src="image" :width="width" :height="height" />
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
        width: {
            type: Number,
            default: 640,
            require: false,
        },
        height: {
            type: Number,
            default: 480,
            require: false,
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
