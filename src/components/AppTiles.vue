<template>
  <div class="tiles">
    <div v-for="(tile, index) in appStore.tilemap.tiles" :key="index" class="tile" :class="{ 'active': tile.id === appStore.activeTileId }" :style="{ background: tile.color }" @click="appStore.setActiveTileId(tile.id)">
      <div>{{ tile.name }}</div>
    </div>
    <div>
      <button @click="appStore.tilemap.addTile()">
        {{ $t('addTile') }}
      </button>
    </div>
  </div>
</template>

<script>
import {mapStores} from 'pinia'
import useAppStore from '@/store/app'
export default {
  name: 'AppTiles',
  computed: {
    ...mapStores(useAppStore)
  },
}
</script>
