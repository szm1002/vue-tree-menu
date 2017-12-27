<template>
  <div id="app">
    <ul>
      <tree-menu v-for="item in treeData" :key="item.id" :model="item"></tree-menu>
    </ul>
  </div>
</template>

<script>
import TreeMenu from './components/TreeMenu'
import './style.css'

const treeData = [
  {
    id: '1',
    name: '文件夹',
    children: [
      {
        id: '11',
        name: '文件'
      },
      {
        id: '12',
        name: '文件夹',
        children: [
          {
            id: '121',
            name: '文件'
          },
          {
            id: '122',
            name: '文件'
          },
          {
            id: '123',
            name: '文件'
          },
          {
            id: '124',
            name: '文件'
          },
          {
            id: '125',
            name: '文件'
          }
        ]
      },
      {
        id: '13',
        name: '文件'
      }
    ]
  },
  {
    id: '2',
    name: '文件'
  },
  {
    id: '3',
    name: '文件夹',
    children: [
      {
        id: '31',
        name: '文件'
      },
      {
        id: '32',
        name: '空文件夹',
        children: []
      }
    ]
  },
  {
    id: '4',
    name: '空文件夹',
    children: []
  },
  {
    id: '5',
    name: '文件夹',
    children: [
      {
        id: '51',
        name: '文件'
      },
      {
        id: '52',
        name: '文件'
      },
      {
        id: '53',
        name: '文件夹',
        children: [
          {
            id: '531',
            name: '文件'
          },
          {
            id: '532',
            name: '文件'
          },
          {
            id: '533',
            name: '文件'
          }
        ]
      },
      {
        id: '54',
        name: '文件'
      },
      {
        id: '55',
        name: '文件'
      }
    ]
  }
]

export default {
  name: 'app',
  data () {
    return {
      treeData: treeData
    }
  },
  components: {
    TreeMenu
  }
}
</script>
