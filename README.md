# jekyll-tagpage-without-plugins

Want a tag page in your Jekyll site on GitHub Pages, where the use of third party plugins is restricted?
You can build it locally, or generate it with this.
Just place three files, and you'll get a tag page that looks like [this](https://yoshum.github.io/PaperSummary/tags/) (a Japanese page, but you can see how it works).

## Usage

1. Copy & paste the following three files in your Jekyll site directory:
  - `tags.html`
    - The tag page that will be deployed as `https://username.github.io/reponame/tags/`
    - The URL and layout are arbitrary; see the frontmatter
  - `assets/tags.json`
    - Currently the path is hard-coded; 
    it must be accessible as `https://username.github.io/reponame/assets/tags.json`
  - `_include/taglist.html`
    - Place it so that `{% include taglist.html %}` in `tags.html` works
2. Commit the changes & push them to the GitHub repository
3. Add posts with tags, and your tag page will be automatically updated

## Restriction

- `tags.json` must be placed in `/assets`
- Tag names must NOT contain the character "#"
