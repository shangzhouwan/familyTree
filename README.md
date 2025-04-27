# familyTree
create my family tree 
---------------------------
参考1：https://github.com/SanichKotikov/relatives-tree
![这是参考1图片](/img/1.png)

  #Installation
  
  `npm i relatives-tree`
  
#Usage

```
import calcTree, { type Node } from 'relatives-tree';

const nodes: Node[] = [
  {
    id: "1",
    gender: "male",
    spouses: [],
    siblings: [],
    parents: [],
    children: [
      { id: "2", type: "blood" },
      { id: "3", type: "blood" }
    ]
  },
  {
    id: "2",
    gender: "female",
    spouses: [],
    siblings: [],
    parents: [{ id: "1", type: "blood" }],
    children: []
  },
  {
    id: "3",
    gender: "male",
    spouses: [],
    siblings: [],
    parents: [{ id: "1", type: "blood" }],
    children: []
  }
];

const tree = calcTree(nodes, { rootId: "1" });

render(tree);
```
参考2: https://github.com/walkerz88/vue-family-tree
![这是参考2图片](/img/2.png)

`npm install vue-family-tree --save`
```
<template>
  <div id="app">
    <VueFamilyTree
      :tree="tree"
      @card-click="cardClick"
    />
  </div>
</template>
```
```
<script>
import VueFamilyTree from 'vue-family-tree';

export default {
  name: 'App',
  components: {
    VueFamilyTree
  },
  data () {
    return {
      tree: [{
        firstPerson: {
          name: 'John Walker',
          image: 'https://picsum.photos/300/300?random=1'
        },
        secondPerson: {
          name: 'Jannet Grem',
          image: 'https://picsum.photos/300/300?random=2'
        },
        children: [{
          firstPerson: {
            name: 'Katia'
          },
          secondPerson: {
            name: 'Oleg'
          },
          children: [{
            firstPerson: {
              name: 'Gleb'
            },
            secondPerson: {
              name: 'Viktoriya'
            },
            children: [{
              firstPerson: {
                name: 'Rim'
              },
              secondPerson: {
                name: 'Natasha'
              }
            },
            {
              firstPerson: {
                name: 'Leonid'
              }
            }]
          },
          {
            firstPerson: {
              name: 'Olga'
            },
            secondPerson: {
              name: 'Nikita'
            }
          }]
        },
        {
          firstPerson: {
            name: 'Vitia'
          },
          secondPerson: {
            name: 'Dasha'
          }
        },
        {
          firstPerson: {
            name: 'Antonio Wild',
            image: 'https://picsum.photos/300/300?random=3'
          },
          secondPerson: {
            name: 'Olivia Olson'
          },
          children: [{
            firstPerson: {
              name: 'Kristina Wild'
            }
          },
          {
            firstPerson: {
              name: 'Alexey Wild'
            }
          },
          {
            firstPerson: {
              name: 'Viktor Wild'
            }
          }]
        }]
      }]
    }
  },
  methods: {
    cardClick (item) {
      console.log(item);
    }
  }
}
</script>
```
参考3:https://github.com/donatso/family-chart

参考4:https://github.com/BenPortner/js_family_tree
![这是参考4图片](/img/4.png)
参考5:https://github.com/daveagp/family-tree

