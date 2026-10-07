# Hobby Site

A personal collection of small web projects built for learning, experimenting, and enjoying the process of making things for the web. The site currently features a utility dashboard combining weather, book discovery, and currency conversion.

## Projects

### Utility Dashboard

An interactive dashboard with three useful tools:

- **Weather:** Look up current conditions for a city, including temperature, humidity, precipitation, and wind.
- **Book library:** Search the Open Library catalogue by title or author and browse matching books.
- **Currency converter:** Convert between USD, INR, EUR, GBP, and JPY using the latest published exchange rates.

## Try it

Once GitHub Pages is enabled for the repository, visit the published site using the URL shown in **Settings → Pages**.

To preview it locally, open the project folder in Visual Studio Code, open `index.html`, and click **Go Live**. You can also run a simple local server from this folder:

```powershell
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deployment

The included GitHub Actions workflow publishes the static site whenever changes are pushed to the `main` branch. To enable it:

1. Push this project to a GitHub repository named `hobby-site`.
2. In the repository, open **Settings → Pages**.
3. Set the build and deployment source to **GitHub Actions**.
4. Push to `main` or start the **Deploy to GitHub Pages** workflow from the Actions tab.

The workflow deploys the static files at the repository root; no build tools or package installation are required.

## Technologies and data sources

- HTML, CSS, and vanilla JavaScript
- [Open-Meteo](https://open-meteo.com/) for geocoding and weather
- [Open Library](https://openlibrary.org/) for book search and cover images
- [Frankfurter](https://www.frankfurter.dev/) for published exchange rates

The dashboard is a static website. It does not require an API key for these services. Exchange rates are the latest rates published by the data provider and may not be real-time market quotes.

## Project structure

```text
.
├── index.html                 # Redirects to the utility dashboard
├── utility_dashboard.html     # Dashboard application
└── .github/
    └── workflows/
        └── deploy-pages.yml   # GitHub Pages deployment workflow
```

## About

This repository is a home for personal hobby projects and web-development experiments. The dashboard is the first project; more can be added as they are built.
