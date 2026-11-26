# Embedding a public Gephi Lite network

Do **not** paste a local `file://` link or a private URL into the public website.

1. Publish the visualization using a supported public share/embed method, or host a compatible export.
2. Obtain its actual public embed URL. Confirm the provider allows framing.
3. Insert the following snippet into a `.qmd` project page, replacing the placeholder with the verified URL:

```html
<div class="network-embed-wrapper">
  <iframe
    src="https://REPLACE-WITH-REAL-PUBLIC-EMBED-URL"
    title="Interactive historical network"
    loading="lazy"
    allowfullscreen>
  </iframe>
</div>
```

Provide a caption describing data provenance, filtering, edge meanings, licensing, and the analytical limitations of the visualization. When possible, add a link to the original visualization and a static fallback figure. Do not deploy the URL placeholder.
