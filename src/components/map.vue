<template>
    <div class="mapComponent">
        <vl-map 
            :load-tiles-while-animating="true" :load-tiles-while-interacting="true" :controls="false"
            data-projection="EPSG:4326" style="height: 100%" min-zoom="10" max-zoom="12">
            
            <vl-view 
                :zoom.sync="zoom" :center.sync="center" :rotation.sync="rotation" 
                :max-zoom="maxZoom" :min-zoom="minZoom">
            </vl-view>

            <vl-layer-tile id="osm">
                <vl-source-osm></vl-source-osm>
            </vl-layer-tile>

            <vl-layer-vector>
                <vl-feature>
                    <vl-geom-point
                        :coordinates="shopCoordinates" 
                    ></vl-geom-point>

                    <vl-style-box>
                        <vl-style-circle :radius="5">
                            <vl-style-fill color="rgba(43, 43, 43, 0.7);"></vl-style-fill>
                            <vl-style-stroke color="black"></vl-style-stroke>
                        </vl-style-circle>
                    </vl-style-box>

                </vl-feature>
            </vl-layer-vector>

            <vl-overlay id="overlay" :position="shopCoordinates">
                <div class="overlayContent">
                    Oto güneş
                </div>
            </vl-overlay>
        </vl-map>
    </div>
</template>

<script>

export default {
    name: "mapAreaComponent",

    data: function(){
        return{
            zoom: 10,
            center: [27.810053595897596, 37.839971797805916],
            rotation: 0,
            geolocPosition: undefined,
            
            shopCoordinates: [27.853116542100842, 37.83866163068258],
            
            minZoom: 9,
            maxZoom: 17
        }
    },

    methods:{

    }
}
</script>

<style scoped>
    .mapComponent{
        width: 100%;
        height: 100%;

        background: rgba(43, 43, 43, 0.7);

        border-right: 6px solid black;

        padding: 1rem;
    }

    .overlayContent{
        color: black;
        background: rgba(43, 43, 43, 0.3);
        font-size: 1rem;
    }

    @media only screen and (max-width: 700px){
        .mapComponent{
            border: none;
            border-bottom: 6px solid black;
        }
    }

</style>