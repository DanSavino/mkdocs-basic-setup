Arquivo extensions.md desta documentação:
```yaml
    # Instalando extensões

    Para adicionar elementos não tradicionais à sua página, você precisará instalar [extensões](https://squidfunk.github.io/mkdocs-material/setup/extensions/)

    ## Configuração Base

    Edite seu arquivo de configuração (mkdocs.yml) e adicione as extensões:
    !!! warning inline end
        Se :exclamation: ==ModuleNotFoundError== :

        É provavelmente porque você não o especificou no arquivo .yml ou o pacote não está disponível em seu **venv**, portanto, você precisará instalá-lo usando **pip install**
    ```yaml
    #Aqui estão as extensões usadas nesta documentação
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
```