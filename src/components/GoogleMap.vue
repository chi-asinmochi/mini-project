<template>
    <div class="google-map" ref="mapDiv"></div>
</template>

<script>
import { Loader } from '@googlemaps/js-api-loader'
import { onMounted, ref } from 'vue';

const gMapAPIKey = 'AIzaSyBOIsnP9f0z4KDGB6QXLXsRkXcwqcMxCLY'

export default {
    name: 'USMap',
    setup() {
        const loader = new Loader({ apiKey: gMapAPIKey })
        const mapDiv = ref(null)
        let map = ref(null)
        onMounted(async () => {
            await loader.load()
            new google.maps.Map(mapDiv.value, {
                center: { lat: 39.0902, lng: -98.55 },
                zoom: 4,

            })
        })
        return {mapDiv}
    }
};
</script>

