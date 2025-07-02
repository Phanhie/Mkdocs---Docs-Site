# **Customizing Your Site with a Theme**

-----

 A good theme makes your documentation easy to read and pleasant to look at. 
 
 In this section, we'll use a popular theme called "Material for MkDocs" to make your site look great.

## **Install Material for MkDocs**

First, you need to install the Material theme. 

Open your Terminal or Command Prompt and type:

```bash
pip install mkdocs-material
```

To check if it's installed, you won't get a direct version for the theme itself, but if the installation finishes without errors, you're good.

## **Update `mkdocs.yml` to Use Material**

Update your MkDocs project to use the Material theme. 

Open your `mkdocs.yml` file and add or update the `theme:` section like this:

```yaml
theme:
  name: material
```

Save the file, and if `mkdocs serve` is running, your site should already be updated.

## **Change Colors & Appearance**

You can easily change the colors of your Material theme. 

In `mkdocs.yml`, under `theme:`, add a `palette:` section:

```yaml
theme:
  name: material
  palette:
    primary: 'indigo'   # Main color for headers, etc.
    accent: 'indigo'    # Color for highlights, links
```

You can pick from many color names (like `red`, `blue`, `green`, `purple`, `amber`, `teal`, etc.). 
Material also automatically styles code blocks nicely. 

If you want to change fonts, you can add `font:` options here too.

## **Add a Logo and Favicon**

Add your own logo and a favicon (the tiny icon in the browser tab). to brand your site.

1.  Place your logo image (e.g., `logo.png`) inside a folder like `docs/img/`.
2.  Place your favicon (e.g., `favicon.ico` or `favicon.png`) directly in the `docs/` folder.
3. Update `mkdocs.yml`:

Example: 

```yaml
theme:
  name: material      
  icon:
    logo: img/logo.png # Path to your logo image
    favicon: favicon.ico # Path to your favicon
```

## **Enable Search**

Material for MkDocs comes with a built-in search feature that works automatically. You don't usually need to do anything extra to enable it once you're using the theme.

## **Add Custom CSS or JavaScript**

If you want to add your own special styling or interactive features, you can.

1.  Create a folder like `docs/css/` and put your `custom.css` file inside.
2.  Create a folder like `docs/js/` and put your `custom.js` file inside.

Then, link them in `mkdocs.yml`:

```yaml
extra_css:
  - css/custom.css
extra_javascript:
  - js/custom.js
```

## **Recap**

You've now learned how to:

- Make your MkDocs site truly your own
- Install a powerful theme
- Change its colors and add your branding with logo and favicon
- Add custom styles or scripts
