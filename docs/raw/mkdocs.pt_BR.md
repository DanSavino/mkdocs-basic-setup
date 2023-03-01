Arquivo mkdocs.yml desta documentação:
```yaml
    site_name: Studying Mkdocs

    nav:
    - Getting Started:
        - Welcome to Mkdocs: index.md
    - Reasons:
        - Reasons for Using Mkdocs: reasons/reasons.md
    - Setup:
        - Basic Mkdocs Setup: setup/setup.md
        - Extensions Setup: setup/extensions.md
        - Plugins Setup: setup/plugins.md 
        - Deploy Setup: setup/deployment.md
    - Raw Pages:
        - Mkdocs yaml file: raw/mkdocs.md
        - Reasons file: raw/raw_reasons.md
        - Setup pages:
            - Basic Setup file: raw/raw_setup.md
            - Extensions file: raw/raw_exten.md
            - Plugin file: raw/raw_plugins.md
            - Deploy file: raw/deploy.md


    repo_name: dansavino/mkdocs-basic-setup
    repo_url: https://github.com/dansavino/mkdocs-basic-setup

    theme:
    name: material
    logo: assets/logo.svg
    favicon: assets/favicon.png
    language: en
    features:
        - navigation.footer
        - navigation.indexes
        - navigation.sections
        - navigation.tabs
        - navigation.top
        - navigation.tracking
        - search.highlight
        - search.suggest
        - content.tabs.link
        - content.code.annotation
        - content.code.copy
        - content.code.annotate

    palette:
        - scheme: default
        primary: deep orange
        toggle:
            icon: material/weather-night
            name: Modo noturno
        - scheme: slate
        primary: deep orange
        toggle:
            icon: material/weather-sunny
            name: Modo claro

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

    plugins:
    - search
    - i18n:
        default_language: en
        docs_structure: suffix
        languages:
            default:
            name: English
            build: true
            pt_BR:
            name: Português
            build: true

    extra:
    social:
        - icon: fontawesome/brands/youtube
        link: http://www.ipsense.com.br/youtube
        - icon: fontawesome/brands/github-alt
        link: https://github.com/
        - icon: fontawesome/brands/facebook
        link: http://www.ipsense.com.br/facebook
        - icon: fontawesome/brands/linkedin
        link: http://www.ipsense.com.br/linkedin
```