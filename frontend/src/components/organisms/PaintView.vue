<template>
    <ImageView :width="width" :height="height" />
</template>

<script>
import ImageView from '@/components/molecules/ImageView'

export default {
    name: 'PaintView',
    components: {
        ImageView,
    },
    datas: function () {
        return {
            width: 640,
            height: 480,
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
