# Astronomer Cloud Documentation

This repository contains all of the code and content that powers Astronomer Cloud [documentation](http://www.cloud-docs.astronomer.io). Documentation for other Astronomer product offerings is stored in the [`docs` repo](https://github.com/astronomer/docs).

## Suggest a Change

If you notice something in our documentation that is wrong, misleading, or could use additional context, the easiest way to make an impact is to create a GitHub issue in this repository. To do so,

1. Go to [Issues](https://github.com/astronomer/cloud-docs/issues)
2. Select **New Issue**
3. Depending on the change you have in mind, select a GitHub issue template.
4. Tell us what you think we can do better by answering the questions in the template.

GitHub issues are triaged by the Astronomer team and addressed promptly. Once you create a GitHub issue, our team may follow up with you with additional questions or comments. Once our team has addressed it, you'll get a notification via GitHub that the issue has been closed and that a change is now live.

## Contribute

To contribute to Cloud docs, fork this repo and create a branch off of `main`. You can do this either directly in the GitHub repository or by clicking the "Edit this page" button on any published document.

Once you have submitted a PR for your changes, Netlify will add a comment to your PR that includes a link to a staging website with your changes.

Small edits and typo fixes don't need to be linked to an issue and should be merged quickly. To get a timely review on a larger contribution, we recommend first creating a detailed GitHub issue describing the problem and linking that within your PR.

Every update to the `main` branch of this repository will trigger a rebuild of our production documentation page at https://www.docs.astronomer.io. It might take a few moments for your merged changes to appear.

### Build Astronomer Docs Locally

If you want to submit a screenshot, GIF, or a new documentation file, we recommend building and testing your documentation change locally. Astronomer Cloud docs are built with [Docusaurus](https://docusaurus.io/), which is our static site generator. Read the following sections for instructions on how to build and test your documentation changes locally with Docusaurus.

#### Installation

Please read the [Docusaurus documentation](https://docusaurus.io/docs/installation#requirements) for information on installing the tools you'll need to work with Docusaurus locally.

#### Local Development

To serve a local version of the Astronomer Cloud docs site with your changes, run:

```console
yarn start
```

This command both builds and serves your local changes. By default, your local build is accessible at `localhost:3000`. From here, any changes you save in your text editor will render on this local site in real time.
