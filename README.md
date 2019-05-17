# Hubcare - Documentation
[![All Contributors](https://img.shields.io/badge/all_contributors-9-orange.svg?style=flat-square)](#contributors)

The Hubcare is an open-source project intended to help free software users and potential contributors to decide which repositories they should use or on which they should contribute. It has an [API](https://github.com/fga-eps-mds/2019.1-hubcare-api) that pulls data from GitHub API and post it to a [Add-on](https://github.com/fga-eps-mds/2019.1-hubcare-plugin).

This repository, in special, is only to containing project [Documentation](https://cjjcastro.gitlab.io/2019-1-hubcare-docs/), which is mostly in Portuguese, due to Brazilian project stakeholders.

For now, the only supported browser is Google Chrome, but NPM may build the Add-on for another browser.

## Technologies

<img src="docs/images/icons/django-rest-framework.png" alt="DjangoRest" height="100" width="110"/><img src="docs/images/icons/chrome.gif" alt="Chrome" height="100" width="110"/><img src="docs/images/icons/vscode.png" alt="Vscode" height="100" width="110"/><img src="docs/images/icons/docker.gif" alt="Docker" height="100" width="110"/><img src="docs/images/icons/github.gif" alt="Github" height="100" width="110"/>

## Installation

### Installing from Chrome Store

Just go to HubCare's page on [Chrome Store](https://chrome.google.com/webstore/detail/hubcare/oilkenamijbelpchecmfpllponcmlcbm) and be happy :winky:

### Running things locally

Wanna see it working on your machine, uh?

Unfortunately, the Add-on code wasn't made for local interaction, you may want to up the API on some deploy service to see it working. But you can still run the API and the Add-On separately if you want.

You'll need have [Docker](https://docs.docker.com/install/) and [Docker-Compose](https://docs.docker.com/compose/install/) installed to see the magic happenning.

And I just know how to do it on a Linux machine. C'mon, Windows is just for gaming, y'know. And MacOS users surely can pay someone to discover how to do it.

#### Running the API

Downloading

```bash
cd ~/your/directory/
git clone https://github.com/fga-eps-mds/2019.1-hubcare-api.git
cd 2019.1-hubcare-api
```

The HubCare API need to send a GitHub username and an API token to authenticate on GitHub API. This is set by environment variables as shown below. You can generate tokens [here](https://github.com/settings/tokens).

```bash
export NAME='username'
export TOKEN='token'
```

There you go!

```bash
docker-compose build
docker-compose up
```

If everything was done right, you now have the HubCare running on your machine. Just navigate to `0.0.0.0:8000` and you should see something. There are services running on ports [8000..8003].

Test it on http://0.0.0.0:8000/hubcare_indicators/fga-eps-mds/2019.1-hubcare-api

#### Running the Add-on

Downloading

```bash
cd ~/your/directory/
git clone https://github.com/fga-eps-mds/2019.1-hubcare-plugin.git
cd 2019.1-hubcare-plugin
```

Building and uping things:

```bash
docker-compose build
docker-compose up
```

This should be enough to turn the service on ( ͡° ͜ʖ ͡°).

Then, open Google Chrome on [chrome://extensions/](chrome://extensions/), activate `Developer mode` on top right corner.

![Developer Mode](docs/images/chromeext.png)

You now shoud see hubcare extension, just activate it.

Just go to some GitHub repo to see it working. I recommend [this one](https://github.com/fga-eps-mds/2019.1-hubcare-api), you can even give it a star! :wink:

#### Running the... Docs?

Okay, I undertand, you don't believe on internet info, wanna see it on your own machine, right?

There you go then

```bash
cd ~/your/directory/
git clone https://github.com/fga-eps-mds/2019.1-hubcare-docs.git
cd 2019.1-hubcare-docs
```

Yeah, now run the docs, girl! Run the docs, boy!

```bash
docker-compose up --build
```

Now, [localhost:8000](localhost:8000) should have a beautyful documentation page.

**Obs:** If you ever want to contribute to docs, make sure to check if the MKDocs is rendering as you wish with the proceed above.


## Deployment

It's set on [GitLab](https://gitlab.com/cjjcastro/2019-1-hubcare-docs), so we can use GitLab CI.

## Built With

[MKDocs - Material](https://squidfunk.github.io/mkdocs-material/getting-started/)

## Contributing

Please make sure to read the [Contribution Guide](.github/CONTRIBUTING.md) before making a pull request. After you've read, don't forget to take an issue!

## License

Do whatever you want with this code, bro/sis. This is under [MIT License](./LICENSE).

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
<table><tr><td align="center"><a href="https://github.com/cjjcastro"><img src="https://avatars0.githubusercontent.com/u/26393787?v=4" width="100px;" alt="Cleber Júnior"/><br /><sub><b>Cleber Júnior</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=cjjcastro" title="Documentation">📖</a> <a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=cjjcastro" title="Code">💻</a></td><td align="center"><a href="https://github.com/Brian2397"><img src="https://avatars1.githubusercontent.com/u/29316265?v=4" width="100px;" alt="Brian Lui"/><br /><sub><b>Brian Lui</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=brian2397" title="Code">💻</a></td><td align="center"><a href="https://github.com/Hiroshi18"><img src="https://avatars0.githubusercontent.com/u/26282955?v=4" width="100px;" alt="Lucas Hiroshi Horinouchi"/><br /><sub><b>Lucas Hiroshi Horinouchi</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=Hiroshi18" title="Code">💻</a> <a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=Hiroshi18" title="Documentation">📖</a></td><td align="center"><a href="https://github.com/RomuloSouza"><img src="https://avatars0.githubusercontent.com/u/36862070?v=4" width="100px;" alt="Rômulo Vinícius de Souza"/><br /><sub><b>Rômulo Vinícius de Souza</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=RomuloSouza" title="Code">💻</a></td><td align="center"><a href="https://github.com/FranciscoHeronildo"><img src="https://avatars1.githubusercontent.com/u/30841230?v=4" width="100px;" alt="Francisco Heronildo"/><br /><sub><b>Francisco Heronildo</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=FranciscoHeronildo" title="Code">💻</a></td><td align="center"><a href="https://github.com/VitorMeirelesOliveira"><img src="https://avatars0.githubusercontent.com/u/37275710?v=4" width="100px;" alt="VitorMeirelesOliveira"/><br /><sub><b>VitorMeirelesOliveira</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=VitorMeirelesOliveira" title="Code">💻</a></td><td align="center"><a href="https://gitlab.com/filipetoyoshima"><img src="https://avatars3.githubusercontent.com/u/29482983?v=4" width="100px;" alt="Filipe Toyoshima"/><br /><sub><b>Filipe Toyoshima</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=filipetoyoshima" title="Documentation">📖</a></td></tr><tr><td align="center"><a href="http://vitor.fer.alves7@gmail.com"><img src="https://avatars1.githubusercontent.com/u/43835325?v=4" width="100px;" alt="Vitor Alves"/><br /><sub><b>Vitor Alves</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=vitorAlves7" title="Code">💻</a></td><td align="center"><a href="https://github.com/Jacoapolinario"><img src="https://avatars3.githubusercontent.com/u/37712347?v=4" width="100px;" alt="Jacó Apolinário"/><br /><sub><b>Jacó Apolinário</b></sub></a><br /><a href="https://github.com/fga-eps-mds/2019.1-hubcare-docs/commits?author=Jacoapolinario" title="Code">💻</a></td></tr></table>

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

## Dev's Recommendation to listen while Coding

 <a href="https://open.spotify.com/playlist/3volu6WNAthdgivf0Ki4U1"><img src="https://mosaic.scdn.co/640/072be8c8070865cdbc15eb91bc78e270bdb2d9955fa3a6cc1848ea743a293d2088046746d1b096089e5288926fadb82f873ccf2b45300c3a6f65fa14e10a7d0572569ee5ec9159ed03c79a8b61b308ec" width="100" height="100" title="SO MUSICAO" alt="SO MUSICAO"></a>
