# Knot Scripts

Personal system administration and maintenance scripts.

## Nginx Scripts
- `scripts/nginx/nginx_config.sh`: Nginx server configuration with SSL setup

## Blog Migration Tools

in `scripts/hexo-migrate-astro`, migrating blog posts from Hexo to Astro format.

### 1. Markdown Converter (`convert_markdown-hexo-to-astro.py`)

This script converts Hexo-formatted markdown files to Astro-compatible format.

#### Features:
- Converts front matter to Astro format
- Renames `date` to `pubDatetime`
- Renames `update/updated` to `modDatetime`
- Removes `mathjax` and `categories` fields
- Extracts the first paragraph before `<!-- more -->` as description
- Removes `<!-- more -->` tags
- Preserves directory structure

### 2. Routes Generator (`generate_routes.py`)

This script generates route mappings for your blog posts.
 Features:
- Creates route mappings for all markdown files
- Generates routes in the format "/old-path": "/posts/new-path"
- Sorts routes alphabetically
- Outputs in a format ready for configuration

Usage:
1. Ensure your markdown files are in the input directory
2. Run the script:

```sh
python generate_routes.py
```

3. Route mappings will be saved in `routes.txt`
