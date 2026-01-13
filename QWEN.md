# Academic Pages GitHub Repository

## Project Overview

This is a fork of the Academic Pages template - a GitHub Pages template specifically designed for personal and professional portfolio-oriented websites. It's built on Jekyll, a static site generator, and is optimized for academic use with features for publications, talks, teaching, and portfolio items.

The template was originally forked from the Minimal Mistakes Jekyll Theme and is currently maintained by Robert Zupko and other contributors. It provides a professional platform for showcasing academic work, publications, talks, and other scholarly activities.

## Key Features

- **Academic-focused content organization**: Collections for publications, talks, teaching, and portfolio items
- **Multiple content types**: Supports blog posts, pages, and academic content
- **Responsive design**: Mobile-friendly layout
- **Multiple theme options**: Available themes include default, air, sunrise, mint, dirt, and contrast
- **Social media integration**: Links to various academic and social platforms
- **Talk location mapping**: Python/Jupyter notebook tools for creating maps of talk locations
- **SEO optimization**: Built-in SEO features
- **Analytics support**: Integration with Google Analytics and other providers

## Directory Structure

- `_config.yml`: Main Jekyll configuration file with site-wide settings
- `_pages/`: Contains main site pages (about, CV, publications, talks, etc.)
- `_posts/`: Blog posts organized by date
- `_portfolio/`: Portfolio items
- `_talks/`, `_publications/`, `_teaching/`: Academic content collections
- `_layouts/`: Jekyll layout templates
- `_includes/`: Reusable HTML components
- `files/`: Static files like PDFs, zip files
- `images/`: Image assets
- `assets/`: CSS, JavaScript, and other assets
- `docker-compose.yaml` and `Dockerfile`: Docker configuration for local development
- `Gemfile`: Ruby dependencies for Jekyll
- `package.json`: Node.js dependencies for build scripts

## Building and Running

### Local Development with Jekyll

1. **Prerequisites**: Install Ruby, Bundler, and Node.js
   - On Linux/WSL: `sudo apt install ruby-dev ruby-bundler nodejs build-essential gcc make`
   - On macOS: `brew install ruby node && gem install bundler`

2. **Install dependencies**:
   ```bash
   bundle install
   ```
   If you encounter permission errors, use:
   ```bash
   bundle config set --local path 'vendor/bundle'
   bundle install
   ```

3. **Serve locally**:
   ```bash
   jekyll serve -l -H localhost
   # Or use bundle exec to ensure correct dependencies:
   bundle exec jekyll serve -l -H localhost
   ```
   The site will be available at `http://localhost:4000`

### Using Docker (Recommended)

1. **Build and run with Docker Compose**:
   ```bash
   chmod -R 777 .  # Make files accessible to Docker container
   docker compose up
   ```
   The site will be available at `http://localhost:4000`

### Using VS Code Dev Container

- Open the repository in VS Code
- VS Code should detect the Dev Container configuration and prompt you to reopen in container
- Or use `F1 → DevContainer: Reopen in Container`
- The site will be automatically hosted at `http://localhost:4000`

## Content Management

### Adding Content

- **Blog Posts**: Add Markdown files to `_posts/` directory with format `YYYY-MM-DD-title.md`
- **Portfolio Items**: Add to `_portfolio/` directory
- **Publications**: Add to `_publications/` directory  
- **Talks**: Add to `_talks/` directory
- **Teaching**: Add to `_teaching/` directory
- **Pages**: Add to `_pages/` directory

### Configuration

- Update `_config.yml` with your personal information, site title, bio, social media links, etc.
- The `author` section contains biographic information and social media links
- Collection settings control how different content types are output

### Talk Map Feature

The repository includes tools to create a map of talk locations:
- `talkmap.py`: Python script to geocode talk locations and create a cluster map
- `talkmap.ipynb`: Jupyter notebook alternative for the same functionality
- These tools read location data from talk markdown files and generate interactive maps

## Development Conventions

- Use YAML front matter in markdown files to define metadata (title, date, permalink, etc.)
- Follow the existing directory structure for different content types
- Use the provided layout templates for consistent styling
- Leverage the built-in collections for academic content organization
- Use the `baseurl` configuration for subdirectory hosting
- The site supports various social media and academic profile links in the author section

## Deployment

The site is designed to be deployed on GitHub Pages:
1. Create a repository named `[your GitHub username].github.io`
2. Push your changes to the main branch
3. Enable GitHub Pages in repository settings
4. The site will be available at `https://[your GitHub username].github.io`

## Maintenance

- Bug reports and feature requests can be submitted via GitHub issues
- The repository is actively maintained by Robert Zupko and other contributors
- For template updates, you may need to manually merge changes due to customization conflicts