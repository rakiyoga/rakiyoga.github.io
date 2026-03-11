# Build & Serve Tool

## Purpose
Local development build and serve commands for the Jekyll site.

## Commands

### Install Dependencies
```bash
bundle install
```

### Serve Locally (with live reload)
```bash
bundle exec jekyll serve --livereload
# → http://localhost:4000
```

### Serve (basic)
```bash
bundle exec jekyll serve
# → http://localhost:4000
```

### Build Production
```bash
bundle exec jekyll build
# Output: _site/
```

### Build with Future Posts
```bash
bundle exec jekyll build --future
```

### CI Build (as in GitHub Actions)
```bash
bundle install && bundle exec appraisal install
bundle exec appraisal jekyll build --future
```

### Clean Build
```bash
rm -rf _site .sass-cache .jekyll-cache
bundle exec jekyll build
```

## Common Issues
| Symptom | Fix |
|---------|-----|
| `Could not find gem` | Run `bundle install` |
| `Address already in use` | Kill existing process or use `--port 4001` |
| CSS changes not reflecting | Delete `.sass-cache/` and rebuild |
| Timezone warning | Change `Germany/Berlin` → `Europe/Berlin` in `_config.yml` |
| Permission denied | Use `bundle exec` prefix |
