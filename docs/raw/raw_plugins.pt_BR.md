Arquivo plugins.md desta documentação:
```yaml
    # Configurando Plugins

    ## Pesquisando por Plugins

    Alguns dos [plug-ins](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins) de terceiros.

    ## Instalando Plugin

    A maioria dos plugins tem uma instalação simples, basta

    Executar ```pip install [plugin-name]```

    E adicionar as dependencias no arquivo de configuração mkdocs.yml

    ``` yaml 
    plugins:
    - nome_plugin:
        - configurações_extras
        - ...
    ```
    ## Configurando plugin de multi-linguagem
    Exemplo de cofiguração do plugin "static-i18n"
    !!! note 
        Este plugin é usado nessa documentação.

    O plugin aceita dois tipos de estruturas para determinar a linguagem, ele pode usar da organização de pastas ou o sufixo do arquivo de conteudo (md).
    The plugin accepts two types of structures to derminate each languague. It can use folder or file suffix.

    Frist install the plug in your virtual enviorment via pip install
    ```
    pip install mkdocs-static-i18n
    ```

    Then configure the plugin. Open mkdocs.yml and edit.
    ```yaml
    plugins:
    - search                                       
    - i18n:                                        # Plugin   
        default_language: en                       # Setting default language 
        docs_structure: suffix                     # How your files will be organized. Default value "suffix"
        languages:                                 
            default:                                 # Setting default language
            name: English                          # Display name 
            build: true
            pt_BR:                                   # Setting other languages 
            name: Português                        # Display name 
            build: true
    ```

    Using:

    ``` { .sh .no-copy }  
    docs_structure: suffix
    ```

    Files structure:
    ``` { .sh .no-copy }
        .
        │  
        ├─ docs/
        │  ├─ top_page1/                     # Subfolder - Top Tab
        │  │  ├─ tab1.md/                    # Markdown file - page content - default language
        │  │  └─ tab1.suffix.md/             # Markdown file - page content - suffix language

    ```
```