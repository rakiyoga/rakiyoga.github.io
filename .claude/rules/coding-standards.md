# Coding Standards

## YAML
- 2-space indentation, no tabs
- Quote strings containing special characters
- Keep `_config.yml` changes minimal and backward-compatible

## HTML / Liquid
- Use semantic HTML5 elements
- Keep Liquid logic in templates, not content files
- Close all HTML tags
- Use `{% include %}` for reusable components

## CSS
- Use theme CSS variables when possible
- Follow Beautiful Jekyll naming conventions
- Mobile-first responsive approach
- No inline styles in content pages (exception: `<summary>` bold styling)

## Markdown
- GitHub Flavored Markdown (GFM) syntax
- One blank line between sections
- Use `---` horizontal rules between major sections
- Use proper heading hierarchy (no skipping levels)

## Images
- Store in `assets/img/` with descriptive filenames
- Always include `alt` attribute
- Use `class="pic"` for standard styling
- Optimize file size before committing

## Git
- Meaningful commit messages (imperative mood)
- Keep commits atomic (one logical change per commit)
- Don't commit `_site/`, `.sass-cache/`, or `Gemfile.lock`
