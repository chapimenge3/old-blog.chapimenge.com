# Official Blog site of Chapi Menge

## Cloning the repository

Because the repo contains submodules, you need to clone it recursively:

```bash
git clone https://github.com/chapimenge3/blog.git
cd blog
git submodule update --init --recursive
```

## Running the site locally

To run the project you need to install hugo. You can find the instructions [here](https://gohugo.io/getting-started/installing/).

```bash
hugo server -D
```

## Adding a new post

The Blog posts are located in the `content/posts` directory. But one feature I added is categories, it means that you filter by category of blog post.

You might be wondering why i am talking about categories, well, it's because the categories are also located in the `content/posts` directory. So, to add a new post, you need to create a new directory in the `content/posts` directory with the name of the category you want to add the post to. Then, create a new file with the name of the post you want to add. The file should have the `.md` extension. But if only the category you want to add the post to doesn't exist, you can create it and add the post in it.

With this in mind, the command to add a new post is:

```bash
hugo new posts/<category>/<post-name>.md
```

## Adding a new category

Adding category is as simple as creating directory/folder inside of `content/posts` directory. The name of the directory/folder will be the name of the category.

## Deploying the site

The site is currently linked to Github pages. So to deploy the site, you need to push the changes to the `main` branch. The site will be automatically deployed to Github pages.

The instruction detail can be found [./.github/workflows/hugo.yml](./.github/workflows/hugo.yml).

## Adding Custom Subdomain name

To add a custom domain name, follow the below steps:

1. Go to Github repository > Settings > Pages > Custom domain
2. Add your custom domain name

## Adding custom Root Domain name

To add a custom root domain name, follow the [Github documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain).

## Google Analytics

To add Google Analytics, follow the below steps:

1. Go to [Google Analytics](https://analytics.google.com/analytics/web/)
2. Create a new property
3. Copy the tracking ID
4. open `config.toml` file
5. Add the tracking ID to the `googleAnalytics` field

## Adding Disqus

To add Disqus, follow the below steps:

1. Go to [Disqus](https://disqus.com/)
2. Create a new site
3. Copy the shortname
4. open `config.toml` file
5. Add the shortname to the `disqusShortname` field

That's it. You are good to go.