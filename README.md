# hugo-website-starter

This is a super minimal website starter to get you up and running quickly with a Hugo website. It makes use of the [hugo-theme-barebones](https://github.com/eimajtrebor/hugo-theme-barebones) project, which is a minimal theme that uses TailwindCSS and Alpine.js.

The theme is a work in progress that provides TailwindCSS, Alpine.js, a handful of starter templates and sensible defaults. You will need to add your own custom templates and configuration to your project to override the defaults.

## Getting started

### Clone this repo

- Make a directory for your website.



- Clone this repository into your new directory.
- Remove the .git directory and initialise your own git repository.

```
% mkdir <name-of-blog>
% git clone git@github.com:eimajtrebor/hugo-blog-starter.git <name-of-website>
% rm -rf .git
% git init
```

### Initialise the project

- Edit the config/_default/module.json if you want a different theme.
- Initialise the project as a Hugo module.
- Pull any submodules into the project (such as the theme).
- Create a package.json using the Hugo module npm command.
- Run npm to install the dependencies.
- Make the content, layouts and data directories.

#### Manual version

```
% hugo mod init github.com/<github-user>/<website-name>
% hugo mod get -u
% hugo mod npm pack
% npm install
% mkdir layouts data content
```

#### Automatic version

- Run the init script.

```
% ./scripts/init github.com/<github-user>/<website-name>
```

### Start creating content

- Create your first post.

```
% hugo new posts/my-first-post.md
```

- Run the npm script to start the website.

```
% npm run hugo-server
```

### Next steps

This is barebones.

You will need to do the some or all of the following:

- Update the config.json.
- Create your own custom templates in the layouts directory.
- Add your own modules (such as JavaScript libraries).
- Add a 404 page.
- Add a robots.txt.


