<template>
    <div class="file-input">
        <form>
            <input type="file" accept="image/*" @change="onSelected" />
        </form>
    </div>
</template>

<script>
export default {
    name: 'FileInput',
    methods: {
        /**
         * 選択された
         */
        onSelected: function (e) {
            const file = e.target.files[0]
            if (!file) { return }

            const reader = new FileReader()
            reader.readAsDataURL(file)
            reader.onload = () => {
                this.$emit('on-load', reader.result)
            }
        }
    },
}
</script>

<style lang="scss" scoped>
</style>