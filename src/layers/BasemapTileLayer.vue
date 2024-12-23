<script setup lang="ts" name="BasemapTileLayer">

import { Layers, Sources } from "vue3-openlayers";
import { Maptiler } from "@/utils/basemaps";

</script>

<template>
    <Layers.OlTileLayer>
        <Sources.OlSourceXyz :url="Maptiler.DarkDataviz" :tileSize="[512, 512]" />
    </Layers.OlTileLayer>
</template>

<style scoped>
</style>
