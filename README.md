# fix-failing-redirects-repro

> Reproduction of https://github.com/n8n-io/n8n-docs/issues/359

1. Install, build and serve:

```sh
npm i
npm run build
npm run serve
```

2. Open http://localhost:8000
3. Click on the `Nodes` link on the top-right corner
4. Middle-click on the `Nodes Library` link → GET fails
5. Middle-click on the `Credential` link → GET fails

To fix:

1. Stop the server.
2. Remove the permalink line from `docs/nodes/nodes-library/core-nodes/Cron/README.md`
3. Remove the permalink line from `docs/nodes/credentials/ActiveCampaign/README.md`
4. Rebuild, re-serve, and re-run the test. → Both GET requests succeed

> **Warning:** Do not confuse `docs/nodes/credentials/ActiveCampaign/README.md` with `docs/nodes/nodes-library/nodes/ActiveCampaign/README.md`