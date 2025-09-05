<h1 align="center">
  <br>
  <a href="https://github.com/Pentulz/Pentulz">
    <img src="https://github.com/Pentulz/.github/blob/main/public/images/logo.png?raw=true" alt="Pentulz" width="200">
  </a>
  <br>

</h1>

<h4 align="center">Orchestrate pentest tools across distributed agents. Unified results, clean UI.</h4>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-AGPL_v3-blue.svg" alt="License: AGPL v3"></a>
  <img src="https://img.shields.io/badge/Status-Alpha-ff8a3a" alt="Project status: Alpha">
  <!-- Add your CI badge when ready:
  <a href="https://github.com/Pentulz/Pentulz/actions"><img src="https://github.com/Pentulz/Pentulz/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  -->
</p>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#quickstart">Quickstart</a> •
  <a href="#links">Links</a> •
  <a href="#authors">Authors</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#license">License</a>
</p>

---

## Key Features

- 🔧 **Tool orchestration**: run pentest tools (e.g., `nmap`) across distributed agents.
- 🧩 **Normalized results**: parse raw outputs into a unified JSON schema.
- 🖥️ **Clear UI**: filterable tables, artifacts links, export (CSV/JSON).

## Quickstart

To start using Pentulz, you need to deploy the backend and frontend. You can do
so by following the instructions in their respective repositories or deploy with
docker compose.

- [Backend](https://github.com/Pentulz/backend)
- [Frontend](https://github.com/Pentulz/frontend)

### Docker compose instructions

Clone this repo or copy [`compose.yaml`](./compose.yaml)

```sh
docker compose up -d
```

You can configure part of the `compose.yaml` using the following variables or
directly modify the file for your use case.

- `APP_CORS_ALLOW_ORIGINS`: Specify which origins are allowed to interact with
  the api. This should match the base URL you plan to use when accessing the
  frontend. (e.g. \["https://pentulz.github.io"\] when deploying to github pages)
- `PUBLIC_API_BASE`: Specify the base url to access the API. (e.g.
  https://api.pentulz.xyz)
- `APP_NAME`: The name of the backend service. This is visible when accessing
  the root of the API or its doc. (e.g. "Pentulz Backend")

When using the default values with compose, the frontend and backend will listen
on any interface. The frontend will only work with localhost due to CORS but
agents should be able to reach the API by manually providing your host's IP.

- [Frontend](http://localhost)
- [Backend](http://localhost:8000)

## Links

- [Project management](https://github.com/orgs/Pentulz/projects/1/views/1)
- [Project report](docs/project-documentation.pdf)
- [Figma mockups](https://www.figma.com/design/nnOXhMv74qXfw7dSoTBIvS/Pentulz?node-id=0-1&t=uH9nQkD28uptY7Ez-1)
- Repositories
  - [Landing page](https://github.com/Pentulz/landing-page)
  - [Frontend](https://github.com/Pentulz/frontend)
  - [Backend](https://github.com/Pentulz/backend)
  - [Agent](https://github.com/Pentulz/agent)
- Deployments
  - [Landing page](https://pentulz.xyz)
  - [Frontend](https://pentulz.github.io/frontend/)
  - [Backend](https://pentulz.up.railway.app/docs)

## Authors

- [Mondotosz](https://github.com/Mondotosz)
- [NATSIIRT](https://github.com/NATSIIRT)
- [Thynkon](https://github.com/Thynkon)
- [Vicolet](https://github.com/Vicolet)

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](LICENSE)
