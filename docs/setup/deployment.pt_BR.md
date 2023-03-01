# Preparando para o *deploy*

Depois que sua pagina estiver pronta. Adicione seu projeto em um repositorio no GitHub para usar o GitHubPages ou até mesmo o ReadTheDocs para hostear o site.


1. Criar seu repositorio no GitHub
2. Inicializar o git no seu projeto local
3. Commitar seu projeto para o repositorio
4. Execute o comando de *deploy* do mkdocs
    ```
    mkdocs gh-deploy
    ```
5. A documentação ficará disponivel dentro de minutos em 
    ```
    https://{usuario-github}.github.io/{repositorio}
    ```

!!! warning 
    Se seu comando mkdocs gh-deploy foi executado com sucesso e sua paginá ainda está offline.
    Verifique as cofigurações do GitHubPages no diretorio e garanta que a fonte é *branch gh-pages*.

Ps: A documentação pode ser importada no ReadTheDocs através da importação do projeto do GitHub.