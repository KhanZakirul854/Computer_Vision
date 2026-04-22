# Setup And Run Guide

## Required Tools

To run this prototype from GitHub, a user needs:

- `git`
- a code editor such as `VS Code`
- a modern browser such as Chrome, Edge, or Safari

## Required Dependencies

This prototype has **no required package dependencies**.

There is:

- no `npm install`
- no `pip install`
- no database setup
- no backend server

## Optional Tools

- VS Code `Live Server` extension

`Live Server` is optional, but it gives a smoother local development workflow.

## Clone From GitHub

```bash
git clone <your-repo-url>
cd <your-repo-folder>
```

## Run Locally

### Option 1: Open Directly

Open:

```text
tagging-ui/index.html
```

in a browser.

### Option 2: Use VS Code Live Server

1. Open the repo in VS Code.
2. Install the `Live Server` extension.
3. Right-click `tagging-ui/index.html`.
4. Choose `Open with Live Server`.

## Files Needed To Run The UI

The prototype uses:

- `tagging-ui/index.html`
- `tagging-ui/styles.css`
- `tagging-ui/app.js`

These files must remain together in the same folder structure.

## Supported Inputs

- `JPG`
- `JPEG`
- `PNG`

Current demo limitation:

- `HEIC` is not supported in this prototype

## Current Functionality

- load a property image
- zoom in and out
- pan around the image
- draw multiple regions on one image
- assign violations to each region
- edit saved violation labels
- export annotation results as JSON

## Known Limitations

- no backend
- no Salesforce connection yet
- no authentication
- no persistent data storage
- no video ingestion in this repo

## Git Push/Pull Notes

This folder can be used normally with git once a remote is connected.

Typical workflow:

```bash
git pull
git add .
git commit -m "Update UI and docs"
git push
```

Push/pull will work after:

- the repo is initialized with git
- a remote GitHub repository is linked
- GitHub authentication is configured on the local machine
