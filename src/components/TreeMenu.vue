<template>
  <li>
    <span @click="toggleFolder">
      <span v-if="isFolder" class="icon" :class="[open ? 'folder-open' : 'folder']"></span>
      <span v-else class="icon file"></span>
      {{ model.name }}
    </span>
    <ul v-if="isFolder" v-show="open">
      <!-- recursive components -->
      <tree-menu v-for="item in model.children" :key="item.id" :model="item"></tree-menu>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'treeMenu',
  props: ['model'],
  data () {
    return {
      open: false
    }
  },
  computed: {
    isFolder: function () {
      return !!this.model.children
    }
  },
  methods: {
    toggleFolder: function () {
      if (this.isFolder) {
        this.open = !this.open
      }
    }
  }
}
</script>
