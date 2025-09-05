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

>[!NOTE]
> The desription of the problem, the solution, process used relative to the course PDG of HEIG-VD is in the [docs/project-documentation.pdf](docs/project-documentation.pdf) file.

---


## Key Features
- **Distributed Tool Orchestration**: Deploy and manage agents across VLANs, cloud VPCs, and on-premises environments to run pentest tools locally within target networks.
- **Unified Result Schema**: Automatically normalize outputs from diverse tools (nmap, gobuster, ffuf, etc.) into a consistent JSON format for streamlined analysis.
- **Centralized Management**: Monitor scan execution, agent status, and collect findings through a secure, scalable backend with PostgreSQL persistence.
- **Intuitive Web Interface**: Explore results through filterable tables, search functionality, and export capabilities (JSON/CSV) with responsive design.
- **Modular Tool Integration**: Add new security tools with just 2 Python files - no architectural changes required.
- **Secure Communication**: All agent-backend communications encrypted via TLS 1.2+ with token-based authentication.
- **Multi-Platform Agents**: Support for Linux x86_64, Windows 64-bit, and containerized deployments (Docker).


## Quickstart

To start using Pentulz, you need to deploy the backend and frontend. You can do
so by following the instructions : 


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

>[!NOTE]
> The deployment in development mode is documented in their respective repositories : 
> - [Backend](https://github.com/Pentulz/backend)
> - [Frontend](https://github.com/Pentulz/frontend)

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

1. Fork the repository you want to contribute to (backend, frontend, agent)
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

>[!NOTE]
> Each repository has its documentation. The contribution workflow is the same for all repositories.
> We will verify that the contribution is relevant to the project and that the code is of good quality.



## License

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](LICENSE)
