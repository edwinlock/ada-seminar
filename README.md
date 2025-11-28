# Academic Seminar Page

A simple Jekyll website for listing academic talks. Update via YAML, host on GitHub Pages.

## Setup for GitHub Pages

1. **Edit the data files**
   - `_data/metadata.yml` - Your seminar info
   - `_data/talks.yml` - Your talks

2. **Push to GitHub and enable Pages**
   - Go to Settings → Pages
   - Set source to `main` branch
   - Your site: `https://username.github.io/repository-name/`

3. **Update `_config.yml` with your URL** (optional)
   ```yaml
   url: "https://username.github.io"
   baseurl: "/repository-name"
   ```

## Local Development

```bash
bundle install --path vendor/bundle
bundle exec jekyll serve
```

Visit `http://localhost:4000`

## Managing Talks

Add to `_data/talks.yml`:

```yaml
- title: "Talk Title"
  speaker: "Speaker Name"
  date: "2025-12-01"         # YYYY-MM-DD format required
  time: "14:00-15:00"        # Use hyphen for time range, spaces optional
  room: "K5.10"
  abstract: "Description here"  # Supports markdown formatting
  video_link: "https://..."  # Optional: Teams/Zoom meeting link
  person_url: "https://..."  # Optional: Speaker homepage
  paper_url: "https://..."   # Optional: Related paper
```

**All fields except `title` and `speaker` are optional.** Abstracts support markdown (links, **bold**, *italic*, etc.).

## Calendar Feature

Each talk has an "Add to Calendar" button that generates an `.ics` file for that specific talk.

**To disable:** Remove the button element from [index.html](index.html:61-63)

## Customization

- **Colors:** Search/replace `#2c5282` in [assets/css/style.css](assets/css/style.css)
- **Layout:** Edit [index.html](index.html)
- **Fonts:** Change in [assets/css/style.css](assets/css/style.css)
