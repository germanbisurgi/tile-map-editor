<template>
  <nav class="nav">
    <div class="container-fluid">
      <div class="nav-items">
        <a class="nav-item" target="_blank" href="https://github.com/germanbisurgi/tiles">
          <i class="bi bi-github" />
          <span class="sr-only">GitHub</span>
        </a>

        <app-language-selector class="nav-item" />
      </div>
    </div>
  </nav>
</template>

<script>
import AppLanguageSelector from "@/components/AppLanguageSelector.vue"
import useAppStore from '@/store/app'
import {mapStores} from 'pinia'


export default {
  name: 'AppNavbar',
  components: {
    AppLanguageSelector
  },
  computed: {
    ...mapStores(useAppStore)
  }
}
</script>
