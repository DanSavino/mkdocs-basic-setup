This webpage plugins.md file.
``` yaml
    # Configuring Plugins 

    ## Searching for Plugins

    Some of 3rd-party [plug-ins](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins)

    ## Installing plugin

    Most of the plugins have a simple installation. 

    Run ```pip install [plugin-name]```

    Then add plugin dependencies to mkdocs.yml file.

    ``` yaml 
    plugins:
    - name_plugin:
        - further_plugin_configuration
        - ...
    ```
    ## Seting multi-language plugin
    For example here is how to set the "static-i18n" plugin
    !!! note 
        This is the plugin used in this documentation

    The plugin accepts two types of structures to derminate each languague. It can use folder or file suffix.

    Primeiro instalar o plugin no ambiente virtual.
    ```
    pip install mkdocs-static-i18n
    ```

    Configurar o plugin no projeto. Abrir mkdocs.yml e editar.
    ```yaml
    plugins:
    - search                                       
    - i18n:                                        # Plugin   
        default_language: en                       # Linguagem padrão 
        docs_structure: suffix                     # Tipo de organização. Valor padrão: "suffix"
        languages:                                 
            default:                                 # Configurar linguagem padrão
            name: English                          # Nome de exibição
            build: true
            pt_BR:                                   # Configurar outra linguagem  
            name: Português                        # Nome de exibição
            build: true
    ```

    Usando:

    ``` { .sh .no-copy }  
    docs_structure: suffix
    ```

    Estrutura dos arquivos:
    ``` { .sh .no-copy }
        .
        │  
        ├─ docs/
        │  ├─ top_page1/                     # Subpasta - Guia superior
        │  │  ├─ tab1.md/                    # Arquivo Markdown- conteúdo da página - linguagem padrão
        │  │  └─ tab1.suffix.md/             # Arquivo Markdown- conteúdo da página - linguagem [suffix]

    ```
```