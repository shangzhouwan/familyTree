# familyTree
create my family tree 
---------------------------
参考1：https://github.com/SanichKotikov/relatives-tree

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

