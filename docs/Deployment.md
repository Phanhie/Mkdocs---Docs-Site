# **Deploy Your MkDocs Site to GitHub Pages**

-----

Once you've built your documentation, you'll want to share it with the world.

Publishing your site online makes it accessible to everyone and GitHub Pages is a fantastic, free option for hosting your MkDocs site directly from your project's code.

Let's walk through the steps involved in this process.

## **Step 1: Create a GitHub Repository**

First, you need a place on GitHub for your project.

1.  Go to `github.com` and log in.
2.  Click the **New** button (or the `+` sign) to create a new repository.
3.  Give your repository a name, like `my-docs-site` (it's often good to match your project folder name).
4.  Choose **Public** so your site can be seen and click **Create repository**.

      **Do not** add a README, `.gitignore`, or license here; you'll add your files soon.

## **Step 2: Initialize Git in Your Project**

TO connect your local MkDocs project to your new GitHub repository: 
1. Open your Terminal or Command Prompt
2. Navigate to your MkDocs project folder ( `cd my-new-docs`)
3. Run these commands one after the other:

```bash
git init   

git remote add origin <Repo-Url>

git add . 

git commit -m "initial commit" 

git push -u origin main 
```

*Remember to replace `<repo-url>` with the actual URL of your GitHub repository.*

## **Step 3: Deploy to GitHub Pages**

Now, your project is on GitHub, deploying is super easy. 

In your project folder, type:

```bash
mkdocs gh-deploy
```

This command does a few things: 
- It builds your entire site (just like `mkdocs build`). 
- Then it pushes the built website files to a special branch on your GitHub repository called `gh-pages`. 
- GitHub Pages then uses this branch to serve your website.

## **Where to View Your Site**

After `mkdocs gh-deploy` finishes, your site should be live. It usually takes a minute or two for GitHub Pages to update.

Your site's address will be in this format:

`https://yourusername.github.io/your-repo-name/`

With `yourusername` replaced with your GitHub username and `your-repo-name` with your repository's name.


**NB:** If your site doesn't show up right away, double-check the URL, make sure your repository is public, and sometimes waiting a few more minutes helps.

## **Recap**

You've successfully: 

- Pushed your MkDocs project to GitHub 
- Deployed it for free on GitHub Pages

Your documentation is now live for everyone to see.
