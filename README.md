# L1nkr - Template
![L1nkr - Simple LinkTree Hugo Theme](https://raw.githubusercontent.com/chrede88/l1nkr/main/images/screenshot.png)

<p align="center">
  <img src="https://github.com/Chrede88/L1nkrTemplate/actions/workflows/testBuild.yml/badge.svg" alt="Template Build">
</p>

L1nkr is a simple LinkTree type [Hugo](https://gohugo.io) theme. The theme is designed mobile-first, with a very intuitive interface.

## Installation

1) Use this template by pressing `Use this template`.
2) Clone your version of the template to your local computer:
```shell
git clone https://github.com/<username>/<reponame>
```
3) Change the module name to match your github repo in `go.mod`.
4) Modify `config/_default/hugo.yaml` and `config/_default/params.yaml` according to the Configuration below.
5) In a terminal/commandline, move to the newly created folder using `cd`.
6) Build a local version of your site by executing `hugo server`. You can see the site by navigating to `localhost:1313`  (actual URL will be outputted in the CLI) in a browser.
7) Add a new image to the `assets/` folder, using the same name as you specified in `params.yaml`.
8) Add a new `icon.png` file to update the favicon. The png file should be 512px by 512px in size.

---

## Features

- Simple LinkTree theme, designed for mobile-first.
- Automatically dark mode (based on system setttings).
- Emoji support for a fun design.
- More than 40 supported brand links.

---

## Configuration

All configuration is done in the two configuration files under `config/_default/`. The URL and site title can be set in `hugo.yaml`, all other parameters are set in `params.yaml`.

`hugo.yaml`:
```yaml
baseURL: 'https://username.github.io/L1nkr'
title: 'L1nkr'
```

`params.yaml`:
```yaml
############################
## Author
############################

author:
  name: "L1nkr"
  image: author.jpeg
  greeting: "A simple LinkTree theme for Hugo :evergreen_tree:"
  icon: ":wave:" # outcomment (or remove) if you don't want to display the emoji


############################
## Links
############################

links:
  - github: https://github.com/username/
  - facebook: https://facebook.com/

############################
## Colunms of Links
############################

# between 2 & 6 columns are supported (both incl)
columns: 3

###############################
## OpenGraph & Twitter Cards
###############################

title: "L1nkr"
description: "Demo site build with L1nkr & Hugo"
images:
  - thumbnail.jpeg
```

Links are defined by the name (i.e. "github" or "facebook"). The names must match one of the supported links, see list below.

### Supported Link Icons
| **Supported Links** | **Supported Links** | **Supported Links** | **Supported Links** |
| --- | --- | --- | --- |
| amazon | apple | bandcamp | bitbucket | 
| bluesky | check-mark | codepen | dev |
| discord | dribbble | email | etsy |
| facebook | flickr | foursquare | github |
| gitlab | google | instagram | keybase |
| kickstarter | link | linkedin | mastodon |
| medium | orcid | patreon | paypal | pinterest |
| reddit | signal | skype | slack |
| snapchat | soundcloud | spotify | stack-exchange |
| stack-overflow | strava | telegram | tiktok |
| tumblr | twitch | untappd | website |
| whatsapp | windows | x-twitter | youtube |


### Custom Link Icons
Users can provide their own icons by placing a `.svg` image in `./assets/icons/` in their own repo. Creating folders when necessary. The image should be as square as possible for the best result. Don't use spaces in the filename!
The background color will be the tailwind color `bg-indigo-500` (#6366f1) unless another color is specified. This can be done by placing the following css snippet in `./assets/css/custom.css`:

```css
.link-nameOfIcon {
  background-color: #6366f1; /* Hex color code */
}
```
Where `nameOfIcon` is be the name of the custom `.svg` file.

---

## Update the Theme Version

The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/Chrede88/L1nkr@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. You can find the releases [here](https://github.com/Chrede88/L1nkr/releases). Please check if any breaking changes are listed under the release you want to update to, before proceeding.

### Danger Zone
If you like to live on the edge, you can get the lastest commit by using the following command:
```shell
  hugo mod get -u github.com/Chrede88/L1nkr
```
This might break your site, as these commits might not have been tested yet.

---

## Deploy on Github Pages
You can very easily deploy your site using Github Pages. Included in this template is a Github Action workflow that will build and deploy your site to Github Pages automatically:+1:

You can find the workflow here `./.github/deploymentWorkflow/buildDeploy.yml`. To use this, move it to `./.github/workflows/`. In this folder you'll find another workflow `testBuild.yml`. This workflow is not needed for anything, you can remove it if you want.

The workflow is already set up and ready to go, but go through it and spend some time to understand what's going on. Otherwise, it'll always be this black box of magic that you can't fix when it breaks!

Last step: Go to Settings -> Pages -> Build and deployment -> Set the Source to "Github Actions".

Next time you publish a release this workflow will build and deploy your site :tada:

Your site will be published to the following URL:
`https://<username>.github.io/<repo>`, where `<username>` and `<repo>` is your Github username and the name of your repository.


