```bash
git init bigbri64.github.io

# > Initialized empty Git repository in /Users/octocat/my-site/.git/

# Creates a new folder on your computer, initialized as a Git repository

## Change directories to the repository.

cd bigbri64.github.io
# Changes the working directory
```

Decide which publishing source you want to use. For more information, see "Configuring a publishing source for your GitHub Pages site."

Navigate to the publishing source for your site. For more information, see "Configuring a publishing source for your GitHub Pages site." For example, if you chose to publish your site from the docs folder on the default branch, create and change directories to the docs folder.

```bash
mkdir docs
# Creates a new folder called docs
cd docs
```

If you chose to publish your site from the gh-pages branch, create and checkout the gh-pages branch.

```bash
git checkout --orphan gh-pages
# Creates a new branch, with no history or contents, called gh-pages, and switches to the gh-pages branch
git rm -rf .
# Removes the contents from your default branch from the working directory
```

---


```bash
git checkout --orphan gh-pages
# Creates a new branch, with no history or contents, called gh-pages, and switches to the gh-pages branch
git rm -rf .
```

```bash
jekyll new --skip-bundle .
# Creates a Jekyll site in the current directory

gem "github-pages", "~> 228", group: :jekyll_plugins


_config.yml

domain: bigbri64.github.io       # if you want to force HTTPS, specify the domain without the http at the start, e.g. example.com
url: https://bigbri64.github.io  # the base hostname and protocol for your site, e.g. http://example.com
baseurl: /docs/                  # place folder name if the site is served in a subfolder

git add .
git commit -m 'Initial GitHub pages site with Jekyll'

git remote add origin https://github.com/bigbri64/bigbri64.github.io.git

git push -u origin gh-pages

```

