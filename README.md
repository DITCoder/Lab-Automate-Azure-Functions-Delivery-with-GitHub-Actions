# CarvedRock Serverless Delivery2

Sample HTTP-triggered Azure Function used in the hands-on lab
**Automate Azure Functions Delivery with GitHub Actions**.

## Contents

- `HttpExample/` — the sample HTTP-triggered function (`function.json` binding + `index.js` code).
- `host.json` / `package.json` — Azure Functions host and Node project files.

## How delivery works

During the lab you fork this repository into your own GitHub account and then:

1. Store a publish profile from the pre-created Azure Function app as the repository secret `AZURE_FUNCTIONAPP_PUBLISH_PROFILE`.
2. Add the deployment workflow (provided in the lab guide) under `.github/workflows/`, and set its `AZURE_FUNCTIONAPP_NAME` to the pre-created function app's name.
3. On every push to `main` (or a manual run), the workflow deploys the function with `Azure/functions-action`.

The live endpoint is `https://<your-function-app-name>.azurewebsites.net/api/HttpExample`.
