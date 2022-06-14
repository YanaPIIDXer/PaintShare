<template>
    <div class="image-view">
        <FileInput @on-load="onReadFile" />
        <div class="paint-area">
            <ImageArea class="image-area" :image="image" :width="width" :height="height" />
            <PaintInput class="paint-input" :enabled="!!image" :width="width" :height="height" />
        </div>
    </div>
</template>

<script>
import FileInput from '@/components/atoms/FileInput'
import ImageArea from '@/components/atoms/ImageArea'
import PaintInput from '@/components/atoms/PaintInput'

export default {
    name: 'ImageView',
    components: {
        FileInput,
        ImageArea,
        PaintInput,
    },
    props: {
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
    data: function () {
        return {
            image: '',
        }
    },
    methods: {
        /**
         * ファイルを読み込んだ
         */
        onReadFile: function (data) {
            this.image = data.image
            this.$emit('on-load', data)
        },
    },
}
</script>

<style lang="scss" scoped>
.image-view {
    .paint-area {
        position: relative;
        left: calc(50% - 320px);
        .image-area, .paint-input {
            position: absolute;
        }
    }
}
</style>
