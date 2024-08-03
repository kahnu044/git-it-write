# Git it Write

_Git it Write_ is a WordPress plugin which allows to publish the markdown files present in a GitHub repository to 
your WordPress site. So with this plugin, whenever the files are added, updated in the repository the WordPress post will be added, updated accordingly.

This plugin is inspired from static site generators like `Jekyll`, `Next.js`, `Gatsby.js` on how content is written is markdown. This is a similar idea for WordPress where markdown data is parsed from GitHub and published as posts.

👓 **Live example:** [Source GitHub repository](https://github.com/vaakash/aakash-web) (`/docs/` folder) to [Posts published](https://www.aakashweb.com/docs/)

📦 **Download/Install:** [Git it write](https://wordpress.org/plugins/git-it-write/) on WordPress plugin repository

⚡ **Getting started:** [Get started](https://www.aakashweb.com/docs/git-it-write/getting-started/) with _Git it Write_. Learn how to write `.md` files and publish posts on WordPress.

This allows people to collaborate with the post, share edits and suggestions in GitHub which when pulled the WordPress post will be updated automatically.

### 🖥️ Example

If a repository has files in the below structure, then below posts will be created (if permalinks are configured and 
the post type supports "hierarchy" i.e. creating posts level by level, like `/pages` in the example below).

**File structure in the GitHub repository:**

    docs/
        guide/
            introduction.md
            getting-started.md
    help/
        faq.md

 **Generated web sides:**

    https://example.com/docs/guide/introduction/
    https://example.com/docs/guide/getting-started/
    https://example.com/help/faq/

### 🎲 What is the use of this plugin ?

* Publish posts using the files in your GitHub repository.
* Write your posts in Markdown format.
* Write your posts on your desktop application (Notepad++, Sublime Text, Visual studio code).
* Collaborate, involve communities on the files in GitHub and publish them on WordPress.
* All the advantages of Git and it's version management system.

### 🚀 Some use cases

* Can be used for documentation posts, FAQs, Wikis etc.
* Write blog posts.
* Any articles which may need community involvement.

### ✨ Features

* Markdown will be processed and post will be published as HTML.
* Images used in the source file will be uploaded to WordPress.
* Relative links are supported.
* Set post properties like post status, title, order, category, tags etc. in the source file itself.
* Webhook support (whenever repository is changed, it updates the plugin to pull the latest changes and publish the posts)
* Add multiple repositories.
* Publish to any post type.
* Posts are published in hierarchical manner if they are under folders. Example: a file `dir1/hello.md` will be posted as `dir1/hello/` in WordPress if the post type supports hierarchy.
* Support for post metadata like setting tags, categories, custom fields.

### ℹ Note

* Only Markdown files will be pulled and published right now
* Posts won't be deleted when it's source file is deleted on GitHub.
* It is preferred to have a permalink structure.
* It is preferred to select a post type which supports hierarchy.
* Images have to present only in `_images` folder in the repository root. Markdown files have to relatively use them in the file.

### 🥗 Recommendation

It is recommended that a permalink structure is enabled in the WordPress site so that, if you have file under `docs/reference/my-post.md` then a post is published like `https://example.com/docs/reference/my-post/`. This will be the result when post type has hierarchy support. They will be posted level by level for every folder in the repository. The folder's post will be taken from the `index.md` file if exists under that folder.

### 🏃‍♂️ Using the plugin

1. Have a GitHub repository where all the source files (markdown files) are maintained (organized in folders if needed the exact structure)
2. In the plugin settings page, click add a new repository.
3. Enter the details of the repository to pull the posts from and under what post type to publish them.
4. Save the settings
5. Click "Pull the posts" and then "Pull only" changes. This will publish posts for all the markdown files.
6. To automatically update posts whenever repository is updated, configure webhook as mentioned in the settings page.

## Links

* [Documentation](https://www.aakashweb.com/docs/git-it-write/)
* [Support forum/Report bugs](https://www.aakashweb.com/forum/)
* [Donate](https://www.paypal.me/vaakash/)

## Installation

1. Extract the zipped file and upload the folder `git-it-write` to the `/wp-content/plugins/` directory.
2. Activate the plugin through the `Plugins` menu in WordPress.
3. Open the admin page from the "Git it Write" link under the settings menu.

## Frequently Asked Questions

Please visit the [plugin documentation page](https://www.aakashweb.com/docs/git-it-write/faq/) for complete list of FAQs.

### When a post is edited in WordPress will that update the file in the GitHub repository ?

No. This plugin won't sync post content. It is a one way update. Only changes made to the GitHub repository will update the posts and not otherwise.

### What all files in the repository will be published ?

All markdown files will be published as posts.

### What are not published ?

Any folder/file starting with `_` (underscore) and `.` (dot) won't be considered for publishing.

### Can I pull posts from a specific branch in the repository ?

Yes, if you want to pull posts from a branch in a repository then you can specify it in the plugin's repository settings page.

### Can I pull posts from a specific folder in the repository ?

Yes, if you want to pull posts from the folder in a repository then you can specify it in the plugin's repository settings page. For example, if a repository has a folder `website/main/docs` and if you want to pull only from docs folder, then you can specify `website/main/docs` in the plugin settings.
