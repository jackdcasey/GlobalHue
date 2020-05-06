<template>
    <div>
        <div class="city" :style="cssProps">
            <span class="citytext">{{city.city}}</span>
            <span class="citytext">{{city.color}}</span>
            <span class="citytext">{{displaytime}}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'City',
    props: {
        city: Object
    },
    data() {
        return {
            displaytime: null
        }
    },
    mounted() {
        let options = { hour: 'numeric', minute: 'numeric', hour12: true, timeZone: this.city.timedata.timezone }
        this.displaytime = new Date().toLocaleString('en-US', options)
    },
    computed: {
        cssProps() {
            return {
                '--bg': this.city.color,
                '--textcolor': this.isDark(this.hexToRgb(this.city.color)) ? '#FFFFFF' : '#000000'
            }
        }
    },
    methods: {
        hexToRgb: function hexToRgb(hex) {
            var result = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(hex);
            return result ? {
                r: parseInt(result[1], 16),
                g: parseInt(result[2], 16),
                b: parseInt(result[3], 16)
            } : null;
        },
        isDark: function isDark(color) {
            return color.r < 160 && color.b < 160 && color.g < 160
        }
    }
}
</script>

<style>
.city {
    width: 100%;
    height: 100px;

    background: var(--bg);

    font-size: xx-large;
    vertical-align: middle;

    display: flex;
    align-items: center;
    justify-content: center;
}

.citytext {
    color: var(--textcolor);
    padding-left: 15px;
    padding-right: 15px;
}

span:first-of-type {
    flex: 1;
}

</style>