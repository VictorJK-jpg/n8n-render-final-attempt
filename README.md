# Deploy n8n on Render

> [!IMPORTANT]
> **View full deployment instructions in the [**Render docs**](https://render.com/docs/deploy-n8n).**

This template defines a [`render.yaml`](https://github.com/render-examples/n8n/blob/main/render.yaml) file you can use to deploy [n8n](https://n8n.io/) on Render. Click **Use this template** in the upper right to copy this template into your account as a new repo.

The `render.yaml` file defines the following resources:

- A web service that pulls and runs the official n8n Docker image
- A Render Postgres database that stores n8n data

Each of the above uses a free instance type by default.

Push these files to your GitHub repo

bash   git add render.yaml Dockerfile .dockerignore
   git commit -m "Add Render deployment config"
   git push

In Render Dashboard:

Click "New +"
Select "Blueprint"
Connect your GitHub repo
Select the repository
Click "Apply"


That's it! Render will:

Create the PostgreSQL database (n8n-postgres-db)
Create the web service (n8n-workflow)
Automatically connect them
Deploy everything
