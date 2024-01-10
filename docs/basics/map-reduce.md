---
sidebar_position: 1
---

# Map Reduce

<!-- Add **Markdown or React** files to `src/pages` to create a **standalone page**:

- `src/pages/index.js` → `localhost:3000/`
- `src/pages/foo.md` → `localhost:3000/foo`
- `src/pages/foo/bar.js` → `localhost:3000/foo/bar` -->

<!-- ## Create your first React Page

Create a file at `src/pages/my-react-page.js`: -->

<!-- ```jsx title="src/pages/my-react-page.js"
import React from 'react';
import Layout from '@theme/Layout';

export default function MyReactPage() {
  return (
    <Layout>
      <h1>My React page</h1>
      <p>This is a React page</p>
    </Layout>
  );
}
``` -->

<!-- A new page is now available at [http://localhost:3000/my-react-page](http://localhost:3000/my-react-page). -->

<!-- ## Create your first Markdown Page -->

<!-- Create a file at `src/pages/my-markdown-page.md`:

```mdx title="src/pages/my-markdown-page.md"
# My Markdown page

This is a Markdown page
```

A new page is now available at [http://localhost:3000/my-markdown-page](http://localhost:3000/my-markdown-page). -->

Data Locality is the potential to move the computations closer to the actual data location on the machines. 

A frame work  used to process mostly a very large set of data in parallel over a bunch of processes.
map reducer comprises of map part which is used to distribute the computation over processes and the reduce part which is used to aggregate the results across distributed processes.

so a map reduce performs the work simultaneously across all processes by dividing it to the servers in the servers, hence utilizing the computation capacity of distributed servers to reduce time of computation.  