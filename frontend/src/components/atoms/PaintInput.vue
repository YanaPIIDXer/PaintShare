<template>
    <div class="paint-canvas">
        <img
            class="input"
            :width="width"
            :height="height"
            v-on="{
                mousemove: onMouseMove
            }"
        />
    </div>
</template>

<script>
export default {
    name: 'PaintInput',
    props: {
        enabled: {
            type: Boolean,
            default: false,
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
    methods: {
        /**
         * マウスが動いた
         */
        onMouseMove: function (e) {
            if (this.enabled && e.buttons) {
                this.$emit('input', {
                    x: e.offsetX,
                    y: e.offsetY,
                })
            }
        }
    },
}
</script>

<style lang="scss" scoped>
.paint-canvas {
    .input {
        opacity: 0;
    }
}
</style>
