<div align="center">
<h1>Minecraft Server Workflow</h1>

This is a GitHub Actions workflow that sets up a Minecraft server and exposes it to the internet using ngrok. It also saves server data to GitHub at regular intervals.

## Usage

To use this workflow, you will need to set up a few things:

1. Copy the contents of `minecraft-server-workflow.yml` into a new workflow file in your repository (e.g. `.github/workflows/minecraft-server.yml`).
2. Set the `NGROK_AUTH_TOKEN` secret in your repository settings. You can get your auth token from the [ngrok dashboard](https://dashboard.ngrok.com/get-started/your-authtoken).
3. Make sure that your Minecraft server jar file is named `paperclip.jar` and is located at the root of your repository.

Once you have set up the workflow, you can run it by pushing to the `main` branch or by triggering it manually from the Actions tab in your repository.

## Notes

- The workflow will run for 2 hours before stopping. You can adjust the loop iteration count in the `Loop for 2 hours and save server data to GitHub` step.
- The workflow will save server data to GitHub at regular intervals, even if it is cancelled. Make sure to cancel the workflow only when you want to stop the server permanently.
- The ngrok URL may take a few seconds to appear in the workflow logs. Be patient!
</div>
