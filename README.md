## This is an example of [Flux](https://fluxcd.io/) usage

### Prerequisites for local installation
- install [kind](https://kind.sigs.k8s.io/docs/user/quick-start/#installation) kubernetes cluster
- Option 1
    - [create a personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)
    - export .env file with GITHUB variables: `export $(cat .env | xargs -0)`
- Option 2
    - [generate ssh key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key) for a specific Github repo 
    - add a [deploy key](https://docs.github.com/en/rest/deploy-keys/deploy-keys?apiVersion=2022-11-28) for the repo

### How to start
- follow along the [instruction](https://fluxcd.io/flux/get-started/)

- Option 2
    - follow [Bootstrap without a GitHub PAT](https://fluxcd.io/flux/installation/bootstrap/github/)
`flux bootstrap git \`
`  --url=ssh://git@github.com/<org>/<repository> \`
`  --branch=<my-branch> \`
`  --private-key-file=<path/to/ssh/private.key> \`
`  --password=<key-passphrase> \`
`  --path=clusters/my-cluster`
