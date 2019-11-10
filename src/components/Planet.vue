<template>
    <div class="planet" :style="stylesOfPlanet">
        <div class="shape" :style="stylesOfShape">
        </div>
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
        marginRight: Number,
        bgColor: String
    },
    data() {
        this.radiusInPx = KmAndPx.km2px(this.radius);
        this.diameterInPx = this.radiusInPx * 2;

        this.marginRightInPx = KmAndPx.km2px(this.marginRight);
        return {
            stylesOfPlanet: {
                // marginRight: this.marginRightInPx + 'px'
            },
            stylesOfShape: {
                width: this.diameterInPx + 'px',
                height: this.diameterInPx + 'px',
                backgroundColor: this.bgColor
            }
        }
    }
}
</script>
<style lang="scss" scoped>
.planet {
    text-align: center;
    margin: 10px;
    .shape {
        border-radius: 50%;
        margin: 0 auto;
        vertical-align: middle;
    }
    .name {
        color: #FFFFFF;
        font-size: 12px;
    }
}
</style>