<p align="center">
  <img src="https://raw.githubusercontent.com/azuki-beans/p7m-apri/main/brand/azuki-beans-logo.svg" alt="azuki-beans" width="260">
</p>

**Azuki Beans** is a small group of friends who build open source software in Python: practical
tools that make public data and everyday Italian bureaucracy a little easier to deal with.

## Projects

| Project | What it does | Try it |
|---|---|---|
| [**coperni**](https://github.com/azuki-beans/coperni) | Air quality forecasts from Copernicus CAMS on a map, for any place in Europe | [coperni.azukibeans.dev](https://coperni.azukibeans.dev) |
| [**p7m-apri**](https://github.com/azuki-beans/p7m-apri) | Open and verify digitally signed `.p7m` files, entirely in the browser | [p7m.azukibeans.dev](https://p7m.azukibeans.dev) |
| [**fatturapa**](https://github.com/azuki-beans/fatturapa) | Zero-dependency parser for Italian electronic invoices (FatturaPA) | [`pip install fatturapa`](https://pypi.org/project/fatturapa/) |

## How we build

- **Python** everywhere, **Django** for web apps, server-rendered HTML with **htmx**.
- **Containers first**: every app ships as a slim image, runs locally with Podman and in the cloud
  unchanged.
- **Serverless when it fits.** Coperni runs entirely on scale-to-zero Google Cloud services: a daily
  Cloud Run Job turns the CAMS forecast into a Parquet file on Cloud Storage, and a stateless Cloud
  Run service reads only the slice each visitor needs with DuckDB over HTTP range requests. No
  database server, no VM. [Read the architecture →](https://github.com/azuki-beans/coperni/blob/main/docs/architecture.md)
- **Open data, cited properly**, and no tracking on our public sites.

Issues and pull requests are welcome on every project.
