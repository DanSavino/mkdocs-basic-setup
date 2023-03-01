# For a Basic Mkdocs Setup

- You can follow the following steps:

## 1. Create a directory folder for your documentation project
!!! Example
    ./projects/client1/documentation


## 2. Create a virtual environment for good practice reasons

!!! Cases

    === "If you have a requirements.txt file"
        Terminal
        ```{ .sh .no-copy }
        $ python3 -m venv mkdocs_venv
        $ source mkdocs_venv/bin/activate
        (mkdocs_venv) $ pip install -r requirements.txt
        ```
        Copy Version
        ```
        python3 -m venv mkdocs_venv
        source mkdocs_venv/bin/activate
        pip install -r requirements.txt
        ```
        

    === "If you are making your own setup from scratch"

        Terminal
        ```{ .sh .no-copy }
        $ python3 -m venv mkdocs_venv
        $ source mkdocs_venv/bin/activate
        (mkdocs_venv) $ pip install mkdocs
        ```
        Copy Version
        ```
        python3 -m venv mkdocs_venv
        source mkdocs_venv/bin/activate
        pip install mkdocs
        ```

## 3. Starting your Mkdocs application
- Open a console on your documentation folder and run:
!!! Example
    Ex: ./projects/client1/documentation

    (mkdocs_venv) ./projects/client1/documentation $ mkdocs new .  

    ```
    mkdocs new . 
    ```
This will start your mkdocs application on the current folder.

## 4. Choosing your theme

For some theme templates and further configuration go to [MkDocs-Themes](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes)

This website theme is [MkDocs-Material](https://squidfunk.github.io/mkdocs-material/)

In order to use a third party theme you will need to install it frist.

```
pip install mkdocs-material
```

Then add it to the main mkdocs configurate file.
Open mkdocs.yml file. 

??? info 
    This file was created on the previous step (  "mkdocs new . "  )
```yaml
site_name: Basic Mkdocs Setup

theme:
    name: material # (1)!
```

1.  Themes also have features installed. In order to add them simply add a feature line in the yaml file.
    ``` yaml
    theme:
        name: material
        features:
            -feature1
            -feature2   
    ```

## 5. Making your page available in dark mode and light mode (Optional)
Open the mkdocs.yml file and add a palette scheme inside theme.
```yaml
theme:
    name: material 
    palette:
        - scheme: default
        primary: deep orange
        toggle:
            icon: material/weather-night
            name: Dark mode
        - scheme: slate
        primary: deep orange
        toggle:
            icon: material/weather-sunny
            name: Light mode
```
- **Ps** : The primary element will represent your main color.

For more options go to [Color-Scheme](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/#color-scheme)

## 6. Creating and edditing new contents  

To create more contents for your documation simply create a MarkDown(md) file. 

In order to edit and create your page open the *md file* and start your documentation following the markdown language pattern. <br>
PS: You can add extensions to add features. For that go to the [Extensions Setup](./extensions.md)

!!! Warning 
    When using :
    ``` yaml
    feature:
        - navigation.tabs 
    ```
    MarkDown file distribuition:
    ``` { .sh .no-copy }
    .
    │  
    ├─ docs/
    │  ├─ top_page1/                     # Subfolder - Top Tab
    │  │  ├─ tab1.md/                    # Markdown file - page content
    │  │  └─ tab2.md/                    # Markdown file - page content
    │  ├─ top_page2/                     # Subfolder - Top Tab
    │  │  ├─ tab1.md/                    # Markdown file - page content
    │  │  └─ tab2.md/                    # Markdown file - page content
    ```
    Configure mkdocs.yml:    

    ``` yaml
    nav:
    - Page1 Name: 
        - Tab1 Name: top_page1/tab1.md   # (1)!
        - Tab2 Name: top_page1/tab2.md  
    - Page2 Name: 
        - Tab1 Name: top_page2/tab1.md   
        - Tab2 Name: top_page2/tab2.md  
    ```

    1.  In this documentation:  
        ``` yaml
        nav:
            - Getting Started:
                - Welcome to Mkdocs: home/index.md
            - Reasons:
                - Reasons for Using Mkdocs: reasons/reasons.md
            - Setup:
                - Basic Mkdocs Setup: setup/setup.md
                - Extensions Setup: setup/extensions.md
        ```
