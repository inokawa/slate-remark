# slate-remark

![check](https://github.com/inokawa/slate-remark/workflows/check/badge.svg)

[remark](https://github.com/remarkjs/remark) plugin to transform remark synthax tree ([mdast](https://github.com/syntax-tree/mdast)) to [slate](https://github.com/ianstormtaylor/slate) document tree, and also slate to remark.

This plugin supports slate 0.50+.

**This is under development. In some usecase this will correctly work but in the others may not work.**

## Install

```
npm install slate-remark
```

## Usage

### Transform remark to slate

```javascript
import unified from "unified";
import markdown from "remark-parse";
import { remarkToSlate } from "slate-remark";

const processor = unified()
  .use(markdown, { commonmark: true })
  .use(remarkToSlate);

const res = processor.processSync(text).result;
console.log(res);
```

### Transform slate to remark

```
Not implemented yet.
```

## Demo

https://inokawa.github.io/slate-remark/