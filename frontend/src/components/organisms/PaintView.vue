<template>
    <div class="paint-view">
        <ImageView :width="width" :height="height" />
    </div>
</template>

<script>
import ImageView from '@/components/molecules/ImageView'
export default {
    name: 'PaintView',
    components: {
        ImageView,
    },
    data: function () {
        return {
            width: 640,
            height: 480,
        }
    },
}
</script>

<style lang="scss" scoped>
</style>
