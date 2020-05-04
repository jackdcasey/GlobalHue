<template>
    <div>
        <div class="city" :style="cssProps">
            <span id="cityName">{{city.city}}</span>
            <span id="cityColor">{{city.color}}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'City',
    props: {
        city: Object
    },
    computed: {
        cssProps() {
            return {
                '--bg': this.city.color
            }
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

span:first-of-type {
    flex: 1;
}

</style>