# Installing extentions 

In order to add non-tradional elements to your page you will need to install [extensions](https://squidfunk.github.io/mkdocs-material/setup/extensions/)

## Minimal Configuration 

Edit your configuration file (mkdocs.yml) and add the extensions:
!!! warning inline end
    If :exclamation: ==ModuleNotFoundError== :

    Its probably because you didn't specify it in the .yml file or the package is not available on your **venv** therefore you will need to install it using **pip install** 
```yaml
#Here are the extensions used in this documentation
markdown_extensions:
  - pymdownx.mark
  - pymdownx.tilde
  - pymdownx.highlight
  - pymdownx.superfences
  - pymdownx.details
  - admonition
  - attr_list
  - pymdownx.tabbed:
      alternate_style: true
  - pymdownx.emoji:
      emoji_index: !!python/name:materialx.emoji.twemoji
      emoji_generator: !!python/name:materialx.emoji.to_svg
```
