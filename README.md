# Route Map

A simple map viewer that shows a driving route between two locations using **Nominatim** (for geocoding) and **OSRM** (for routing).

## 🚀 Setup (GitHub Pages)

1. Fork or upload this repo to your GitHub account.
2. Go to **Settings → Pages**.
3. Under "Branch", select `main` and `/ (root)`, then Save.
4. Your site will be live at:
   ```
   https://<your-username>.github.io/route-map/
   ```

## 🔗 Usage

Append `from` and `to` parameters in the URL:

```
https://<your-username>.github.io/route-map/?from=New York&to=Boston
```

This will render the route between New York and Boston.

## 🖥️ Embedding in Appian

Use a!webContentField with:

```apian
a!webContentField(
  source: concat(
    "https://<your-username>.github.io/route-map/?from=",
    urlencode(local!from),
    "&to=", urlencode(local!to)
  ),
  height: "MEDIUM",
  showBorder: true
)
```

