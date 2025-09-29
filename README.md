# friendsofbramleypark.com

## Develop your Site

1) Install Hugo
```shell
sudo apt update && sudo apt install hugo
```
2) Clone your repo to your local computer:
```shell
git clone https://github.com/Friends-of-Bramley-Park/friendsofbramleypark.com
```
3) Modify `config/_default/hugo.yaml` and `config/_default/params.yaml` according to your needs. Find more info on the theme [wiki](https://github.com/chrede88/L1nkr/wiki/Configuration).
4) Build and run a local version of your site. Run at the root of the repository: `hugo server --baseURL http://localhost:1313`.
5) See the site by navigating to `http://localhost:1313` in a browser. (As you make changes to the codebase, the site will auto-regenerate).
6) Push your changes to Github - the site will automatically rebuild and redeploy. (see more below).

---

## Deploy on Github Pages
The site is deployed to Github Pages by means of a Github Action workflow that automatically builds and deploys the site.

The site will be published to the following URL: `https://friendsofbramleypark.com`

You can find the workflow config here: `.github/workflows//buildDeploy.yml`.

Enabling the workflow (one-time setup only):

Go to Settings -> Pages -> Build and deployment -> Set the Source to "Github Actions".

Next time you push a change to the repo, this workflow will build and deploy the site.

---

## Configuration

See the [wiki](https://github.com/chrede88/L1nkr/wiki) for all info about configuration.

---

## Update the Theme Version

The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/chrede88/L1nkr@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. You can find the releases [here](https://github.com/chrede88/L1nkr/releases). Please check if any breaking changes are listed under the release you want to update to, before proceeding.

---


