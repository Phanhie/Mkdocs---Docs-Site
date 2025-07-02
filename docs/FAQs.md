# **Frequently Asked Questions**

---

Here are some common questions and helpful tips for using MkDocs.

??? "**Why isn't my new page showing in the sidebar?**"
    If you create a new Markdown file (.md) but it doesn't appear in your site's navigation, it's likely because you haven't added it to your mkdocs.yml file.

    **Solution:**  
    Open `mkdocs.yml` and make sure your new page is listed under the nav: section. For example:

    ```yaml
    nav:
    - Home: index.md
    - My New Page: my-new-page.md
    ```


??? "**How do I add images or assets?**"

    You can place images (like .png, .jpg) or other files (like PDFs) directly inside your docs/ folder, or in subfolders within docs/ (e.g., docs/images/).

    **Solution:**  
    Use relative paths in your Markdown:

    | Image Location | Markdown Syntax |
    |----------------|------------------|
    | Same folder as .md | `![Alt Text](image.png)` |
    | Inside docs/images/ and .md is in docs/ | `![Alt Text](images/image.png)` |
    | .md is in docs/section/ and image in docs/images/ | `![Alt Text](../images/image.png)` |


??? "**Can I use HTML inside Markdown files?**"

    Yes, you can! Markdown is designed to work well with HTML. If Markdown doesn't offer a specific formatting option, you can often just write standard HTML directly within your .md files.

    **Example:**

    ```html
    <div style="color: blue; padding: 10px; border: 1px solid blue;">
    This content is inside an HTML div!
    </div>
    ```

??? "**How do I update my deployed site?**"

    When you make changes to your documentation (add pages, edit content, change mkdocs.yml), you need to "re-deploy" them for the changes to appear online.

    **Solution:**  
    1. Save all your changes locally.  
    2. Commit your changes to Git:  
    ```bash
    git add .
    git commit -m "Your update message"
    ```  
    3. Run the deploy command:  
    ```bash
    mkdocs gh-deploy
    ```

    This will build your updated site and push it to GitHub Pages.


??? "**How do I add collapsible sections or tabs?**"

    The Material for MkDocs theme supports many advanced features, including collapsible sections and tabs. 

    These require enabling specific Markdown extensions in your mkdocs.yml.

    **Solution:**  
    Enable extensions in mkdocs.yml:

    ```yaml
    markdown_extensions:
    - pymdownx.details
    - pymdownx.superfences
    - pymdownx.tabbed
    ```

    **Use this syntax in your .md files:**

    **Collapsible Section:**

    ```markdown
    ??? "Click to expand"
        This content is hidden until clicked.
    ```

    **Tabbed Content:**

    ```markdown
    === "Tab 1"
        Content for tab 1.

    === "Tab 2"
        Content for tab 2.
    ```

??? "**Is MkDocs good for API documentation?**"

    Yes, MkDocs, especially when combined with the Material for MkDocs theme, is a great choice for API documentation.

    **Solution:**  
    Look into plugins like `mkdocs-openapi` or `mkdocs-swagger-ui-plugin` to display your API definitions beautifully.

??? "**Where can I learn more?**"
    The best places to get more in-depth information are the official documentation sites for MkDocs and the Material for MkDocs theme.

    **Solution:**  
    
    - [MkDocs Official Docs](https://www.mkdocs.org/)
    - [Material for MkDocs Docs](https://squidfunk.github.io/mkdocs-material/)
