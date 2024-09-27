# Gitorial mdBook Template

A starting template for building an mdBook using Gitorial.

## Features

This template is a lightly modified version of the default `mdBook` template.

- Custom CSS to provide:
	- Two column layout with dual scroll and adjusted padding.
	- Reduced footprint of the nav buttons.
	- Tabs for accessing code in the Gitorial.
	- Color highlighting for filenames.
- Custom JS to support code navigation.
- Github workflow for rendering and publishing the mdBook automatically.
- Github repository link in the `book.toml` file.

## Usage

When using the [`gitorial-sdk/cli`](https://github.com/gitorial-sdk/cli), you can directly target a branch based on this template.

For example, if the `mdbook` branch of a Gitorial repo is this template, then you can simply run:

```sh
gitorial-cli mdbook -p /path/to/rust-state-machine -i gitorial -o mdbook
```

The content of the `/src/` folder will be updated with the latest content from the `gitorial` branch.

## Deployment

Update the `.github/workflows/mdbook.yml` and change the `branches` to match the branch where this template is held. It is configured to `master` to deploy the book for this template repo, but normally you would want to change it to `mdbook`.

Then, in your GitHub settings, under `Pages`, update the source to `GitHub Actions`.

Once you push to your mdBook branch, deployment should automatically take place.
