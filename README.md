# fix-failing-redirects-repro

> Reproduction of https://github.com/n8n-io/n8n-docs/issues/359

1. Install, build and serve:

```sh
npm i -g anywhere
npm i
npm run build
npm run serve
```

2. Open http://localhost:8000
3. Click on the `Nodes` link on the top-right corner
4. Middle-click on the `Nodes Library` link → fails
5. Middle-click on the `Credential` link → fails