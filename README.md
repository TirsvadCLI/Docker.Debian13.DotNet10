[![][Docker Pulls Shield]][Docker Pulls Url]
[![][Docker Stars Shield]][Docker Stars Url]
[![][License Shield]][License Url]

# ![Logo] TirsvadCLI Docker image — Debian 13 + .NET 10

Lightweight `debian:13-slim` image with the .NET 10 SDK installed. Suitable as a base for CLI tooling that requires .NET 10.

## ⚡ Quick start

Prerequisites:
- Docker
- Docker Compose (v2+)

Download:
```bash
docker pull tirsvad/tirsvadcli_debian13_dotnet10:latest
```

Build from source:
```bash
git clone https://github.com/TirsvadCLI/TirsvadCLI.Docker.Debian13.DotNet10.git
cd TirsvadCLI.Docker.Debian13.DotNet10
docker compose build --pull --no-cache
```

Run a container:
```bash
docker run --rm -it tirsvad/tirsvadcli_debian13_dotnet
```

## 🧱 Base image
- `debian:13-slim`
- `mcr.microsoft.com/dotnet/aspnet:10.0` - official Microsoft .NET 10 ASP.NET runtime image.
- `mcr.microsoft.com/dotnet/sdk:10.0` - official Microsoft .NET 10 SDK image.
- Common dependencies for .NET applications
 
## 🛠️ Troubleshooting

If the build fails, run with plain logs to see diagnostics:

```bash
docker compose build --no-cache --progress=plain
```

Common issues:
- Network/download failures when adding Microsoft packages — retry the build.
- Missing native dependencies — check the `apt` step output in the Dockerfile.

## 📁 Files of interest
- `Dockerfile` — builds Debian 13 + .NET 10 image
- `docker-compose.yml` — minimal compose file for local development

## 📜 License
This project is licensed under the [License Url].

<!-- Links -->
[Docker Pulls Shield]: https://img.shields.io/docker/pulls/tirsvad/tirsvadcli_debian13_dotnet10?style=flat-square
[Docker Pulls Url]: https://hub.docker.com/r/tirsvad/tirsvadcli_debian13_dotnet10 "Docker Hub Pulls"	
[Docker Stars Shield]: https://img.shields.io/docker/stars/tirsvad/tirsvadcli_debian13_dotnet10?style=flat-square
[Docker Stars Url]: https://hub.docker.com/r/tirsvad/tirsvadcli_debian13_dotnet10 "Docker Hub Stars"

[Logo]: https://raw.githubusercontent.com/TirsvadCLI/Logo/main/images/logo/32x32/logo.png

[License Shield]: https://img.shields.io/badge/License-AGPLv3-blue.svg
[License Url]: ./LICENSE "GNU AGPLv3 License"
