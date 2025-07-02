# **Creating Pages in MkDocs**

-----

In MkDocs, your documentation is made of pages. Each page is a simple text file written in Markdown. 

This guide shows you how to create new pages and get them to show up on your website.

## **Create a New Page**

To create a new page, create a new file ending with `.md` (Markdown) inside your `docs/` folder.

**For example;**

1. Open your `my-new-docs` project folder
2. Go into the `docs` folder
3. Create a new file named `getting-started.md`.

## **Link Your Page in `mkdocs.yml`**

After creating a new `.md` file, it won't show up on your site until you link it to MkDocs. 

You can do this in the `mkdocs.yml` file.

1. Open `mkdocs.yml`
2. Find or add the `nav:` section. 
3. Add your new page there.

For Example:

```yaml
nav:
  - Getting Started: getting-started.md 
```

## **Example of Adding Multiple Pages**

You can add as many pages as you need. 

Just create the `.md` files and list them in `nav:`.

```yaml
nav:
  - Homepage: index.md
  - Installation: installation.md
  - Features: features.md
  - Usage: usage.md
  - FAQs: faqs.md
```

## **Text and Formatting in Pages**

You can content to your pages using markdown. 

You can add texts, images, links, videos, lists, and a lot more. 

If you do not know how to format with markdown you can use the folowing beginner guides to get started 

- Markdown For Beginners:[Markdown for beginners](https://medium.com/@Phanhie/markdown-for-beginners-3d92946f9689)

- Markdown Guide: [Markdown Guide](https://www.markdownguide.org/)



## **Organizing Pages into Folders**

For bigger sites, you can put related pages into subfolders inside `docs/`.

Example: `docs/features/cool-feature.md`

Then, update your `mkdocs.yml` `nav:` to show this structure:

```yaml
nav:
  - Homepage: index.md
  - Features:
    - Cool Feature: features/cool-feature.md 
    - Another Feature: features/another-feature.md
  - FAQs: faqs.md
```

## **Recap**

Now you know:

- How to create new pages
- Link them in your site's menu
- Add basic content and formatting
- You can also organize your pages into folders for a cleaner site
