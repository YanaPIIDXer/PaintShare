<template>
    <div class="image-view">
        <FileInput @on-load="onReadFile" />
        <ImageArea :image="image" :width="width" :height="height" />
    </div>
</template>

<script>
import FileInput from '@/components/atoms/FileInput'
import ImageArea from '@/components/atoms/ImageArea'

export default {
    name: 'ImageView',
    components: {
        FileInput,
        ImageArea,
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

</style>
