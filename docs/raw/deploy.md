This webpage deployment.md file.
```yaml
    # Preparing for deployment

    After you have a fully working page. Commit your project to GitHub and use GitHubPages or even ReadTheDocs to host it.

    1. Create your GitHub repositorie
    2. Inicialize git in your project page
    3. Commit your project to GitHub main branch
    4. Run mkdocs deploy command 
        ```
        mkdocs gh-deploy
        ```
    5. Your documentation will be available in a couple minutes on 
        ```
        https://{your-github-user}.github.io/{repositorie}
        ```

    !!! warning 
        If mkdocs gh-deploy ran successfully and your page is not online.
        Check GitHubPages settings ou your repositorie. Make sure your source is *branch gh-pages*.

    Ps: The documentation can be add to ReadTheDocs by importing your GitHub project.
```