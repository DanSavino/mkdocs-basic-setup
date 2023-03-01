Arquivo setup.md desta documentação:
```yaml
    # Configuração básica do Mkdocs

    - Você pode seguir os seguintes passos:

    ## 1. Crie uma pasta de diretório para seu projeto de documentação
    !!! Exemplo
        ./projects/client1/documentation


    ## 2. Crie um ambiente virtual por motivos de boas práticas

    !!! casos

        === "Se você tiver um arquivo requirements.txt"

            ```
            $ python3 -m venv mkdocs_venv
            $ source mkdocs_venv/bin/activate
            (mkdocs_venv) $ pip install -r requirements.txt
            ```
            

        === "Se você está fazendo sua própria configuração do zero"

            ```
            $ python3 -m venv mkdocs_venv
            $ source mkdocs_venv/bin/activate
            (mkdocs_venv) $ pip install mkdocs
            ```

    ## 3. Iniciando sua aplicação Mkdocs
    - Abra um console em sua pasta de documentação e execute:
    !!! Exemplo
        Ex: ./projects/client1/documentation

        (mkdocs_venv) ./projects/client1/documentation $ mkdocs novo .

        ```
        mkdocs novo.
        ```
    Isso iniciará seu aplicativo mkdocs na pasta atual.

    ## 4. Escolhendo seu tema

    Para alguns modelos de tema e configurações adicionais, vá para [MkDocs-Themes](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes)

    O tema deste site é [MkDocs-Material](https://squidfunk.github.io/mkdocs-material/)

    Para usar um tema de terceiros, você precisará instalá-lo primeiro

    ```
    pip instalar mkdocs-material
    ```

    Em seguida, adicione-o ao arquivo de configuração principal do mkdocs.
    Abra o arquivo mkdocs.yml

    ??? info
        Isso arquivo foi criado na etapa anterior
    ```yaml
    site_name: Configuração básica do MKdocs

    tema:
        nome: material
    ```

    ## 5. Disponibilizando sua página no modo escuro e no modo claro (opcional)
    Abra o arquivo mkdocs.yml e adicione um esquema de paleta dentro do tema.
    ```yaml
    tema:
        nome: material
        paleta:
            - esquema: default
            primário: deep orange
            alternar:
                ícone: material/weather-night
                nome: Modo Escuro
            - esquema: slate
            primário: deep orange
            alternar:
                ícone: material/weather-sunny
                nome: Modo Claro
    ```
    - **Ps** : O elemento primário representará sua cor principal.

    Para mais opções, vá para [Esquema de cores](https://squidfunk.github.io/mkdocs-material/setup/change-the-colors/#color-scheme)

    ## 6. Criação e edição de novos conteúdos

    Para criar mais conteúdo para sua documentação, basta criar um arquivo MarkDown(md).

    Você pode definir sua página inicial e também as páginas e a ordem que serão exibidas no lado esquerdo da documentação.

    Para isso abra seu arquivo mkdocs.yml e defina os seguintes padrões:
    ```yaml
    nav:
        - Razões para usar o Mkdocs: index.md
        - Configuração básica do Mkdocs: setup.md
        # - Nome da aba: $pathtofile
    ```
    Para editar e criar sua página, abra o *arquivo md* e inicie sua documentação seguindo o padrão de linguagem markdown. <br>
    PS: Você pode adicionar extensões para adicionar recursos. Para isso, vá para [Configuração de extensões](./extensions.pt_BR.md)

    !!! Warning
        Ao usar:
        ``` yaml
        feature:
            - navigation.tabs 
        ```
        Distribuição adequada do arquivo md:
        ``` { .sh .no-copy }
        .
        │
        ├─ documentos/
        │ ├─ top_page1/ # Subpasta - Guia superior
        │ │ ├─ tab1.md/ # Arquivo Markdown - conteúdo da página
        │ │ └─ tab2.md/ # Arquivo Markdown - conteúdo da página
        │ ├─ top_page2/ ## Subpasta - Guia Superior
        │ │ ├─ tab1.md/ # Arquivo Markdown - conteúdo da página
        │ │ └─ tab2.md/ # Arquivo Markdown - conteúdo da página
        ```
        Configurar mkdocs.yml:

        ``` yaml
        nav:
        - Introdução: # (1)!
            - "Nome da guia": top_page1/welcome.md
            - Razões para usar o Mkdocs: top_page1/reasons.md
        - Configurar:
            - Configuração básica do Mkdocs: setup/setup.md # (2)!
            - Configuração de extensões: setup/extensions.md
        ```

        1. Este será o nome da página.
        2. Este será o nome da guia: caminho para o arquivo md.
```