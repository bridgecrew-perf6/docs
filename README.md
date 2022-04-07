# LabDAO Docs

This repository powers [`docs.labdao.com`](https://docs.labdao.com). It pulls together all LabDAO/OpenLab documentation together into a single site using [Docusaurus](https://docusaurus.io/).

### Writing documentation

We've established some conventions around writing documentation that make it easy to integrate new projects' docs into this repository and deploy those docs to `docs.labdao.com`. Here's what you need to know:
* All documentation should live in a folder named `docs/` in the root of your repository.
* When making references between documentation files, [use relative paths](https://docusaurus.io/docs/docs-markdown-features#referencing-other-documents).
* Each Markdown page should have a [front matter](https://docusaurus.io/docs/api/plugins/@docusaurus/plugin-content-docs#markdown-front-matter) section at the beginning, which at minimum should define the document's `title` and `description`.
* Any documents that you want to reference repeatedly throughout your documentation, but do not want to be standalone pages, should be in `_partials/` folders. You can have as many of these folders as you want, scattered throughout your `docs/` directory, but they all should be named `_partials/`.

To add your repository's documentation to `docs.labdao.com`, make a pull request adding your repository as a Git submodule inside of this repository's `docs/` folder.


### Development

```
$ yarn
$ yarn start
```
This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.


### Build

```
$ yarn build
```


This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

This repository is deployed using [Vercel](https://vercel.com/), which has a Docusaurus V2 template. Just create a new Vercel project, connect it to this repository, and click deploy, and you're off to the races!
