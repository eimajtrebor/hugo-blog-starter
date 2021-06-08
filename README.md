# hugo-blog-starter

This is a super minimal blog starter to get you up and running quickly with a Hugo blog that uses TailwindCSS. The theme is a work in progress at the moment and just pulls in the TailwindCSS library. You will need to add your own custom templates to your project's layouts directory.

## Getting started

### Clone this repo

- Make a directory for your blog.
- Clone this repository into your new directory.
- Remove the .git directory and initialise your own git repository.

```
% mkdir <name-of-blog>
% git clone git@github.com:eimajtrebor/hugo-blog-starter.git <name-of-blog>
% rm -rf .git
```

### Initialise the project

- Initialise the project as a Hugo module.
- Pull any submodules into the project (such as the theme).
- Create a package.json using the Hugo module npm command.
- Run npm to install the dependencies.
- Make the content, layouts and data directories.

#### Manual version

```
% hugo mod init github.com/<github-user>/<blog-name>
% hugo mod get -u
% hugo mod npm pack
% npm install
% mkdir layouts data content
```

#### Automatic version

- Run the init script.

```
% ./scripts/init github.com/<github-user>/<blog-name>
```

### Start blogging

- Create your first post.

```
% hugo new posts/my-first-post.md
```

- Run the npm script to start the blog.

```
% npm run hugo-server
```

### Next steps

This is barebones.

You will need to do the some or all of the following:

- Update the config.json.
- Create custom template in the layouts directory.
- Add your own modules (such as alpine.js).
- Add a 404 page.
- Add a robots.txt.


