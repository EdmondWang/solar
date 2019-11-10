<template>
    <div class="planet" :style="styles">
        <span class="name">{{name}}</span>
    </div>
</template>
<script>
import KmAndPx from '../utils/KmAndPx';

export default {
    name: 'Planet',
    props: {
        name: String,
        radius: Number,
        bgColor: String
    },
    data() {
        this.radiusInPx = KmAndPx.km2px(this.radius);
        this.diameterInPx = this.radiusInPx * 2;

        return {
            styles: {
                width: this.diameterInPx + 'px',
                height: this.diameterInPx + 'px',
                lineHeight: this.diameterInPx + 'px',
                backgroundColor: this.bgColor
            }
        }
    }
}
</script>
<style lang="scss" scoped>
    $box-model: border-box;
    .planet {
        box-sizing: $box-model;
        border-radius: 50%;
        text-align: center;
        vertical-align: middle;
        .name {
            color: #FFFFFF;
        }
    }
</style>