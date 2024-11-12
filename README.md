# L1nkr - Template

This is the theme template repository! **Please** follow the installation instructions below.
If you're looking for the actual theme repository, follow this [link](https://github.com/chrede88/L1nkr).

## Installation

1) Use this template by pressing `Use this template`. **Don't fork this repository!**
2) Wait 20s-30s and update the page. The `Clean Template` workflow will run automatically, creating/poplutating files based on your Github user.
3) Add a LICENSE to your repository.
4) Clone your version of the template to your local computer:
```shell
git clone https://github.com/<username>/<reponame>
```
5) Modify `config/_default/hugo.yaml` and `config/_default/params.yaml` according to your needs. Find more info on the theme [wiki](https://github.com/chrede88/L1nkr/wiki/Configuration).
6) Build a local version of your site by executing `hugo server`, at the root of the repository. You can see the site by navigating to `localhost:1313` (actual URL will be outputted in the CLI) in a browser.

---

## Features

- Simple LinkTree theme, designed for mobile-first.
- Automatically dark mode (based on system setttings).
- Emoji support for a fun design.
- More than 50 supported brand links.
- Healthcheck endpoint (/healthcheck.json).

---

## Configuration

See the [wiki](https://github.com/chrede88/L1nkr/wiki) for all info about configuration and how to easily deploy to Github Pages.

---

## Update the Theme Version

The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/chrede88/L1nkr@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. You can find the releases [here](https://github.com/chrede88/L1nkr/releases). Please check if any breaking changes are listed under the release you want to update to, before proceeding.