<template>
    <div class="image-view">
        <FileInput  @on-load="onReadFile" />
        <ImageArea :image="image" />
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
        },
    },
}
</script>

<style lang="scss" scoped>

</style>
