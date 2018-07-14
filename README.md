# Local

- Follow guide from https://jekyllrb.com/docs/quickstart/

# How to publish jekyll to github pages

1.  Modify Gemfile
    - remove the `gem "jekyll"` above and uncomment `gem "github-pages", group: :jekyll_plugin`.
2.  Follow guide from https://www.youtube.com/watch?v=fqFjuX4VZmU
    - change `_config.yml`: set `baseurl`
    - `git add .` and `git commit -m 'some commit msg'`
    - push to `gh-pages` branch
