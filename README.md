# hugo-website-starter

This is a super minimal website starter to get you up and running quickly with a Hugo website. It makes use of the [hugo-theme-barebones](https://github.com/eimajtrebor/hugo-theme-barebones) project, which is a minimal theme that uses TailwindCSS and Alpine.js.

The theme is a work in progress that provides TailwindCSS, Alpine.js, a handful of starter templates and sensible defaults. You will need to add your own custom templates and configuration to your project to override the defaults.

## Getting started

### Clone this repo

- Make a directory for your website.

```
% mkdir <name-of-website>
```

- Clone this repository into your new directory.

```
% git clone git@github.com:eimajtrebor/hugo-website-starter.git <name-of-website>
```

- Remove the .git directory and initialise your own git repository.

```
% cd <name-of-website>
% rm -rf .git
% git init
```

- Add the files and perform an initial commit.

### Update the configuration

Review the initial configuration and make any changes. You can return the configuration once the site is up and running.

#### config.json

- Edit `config/_default/config.json`.
- Add the base URL, language code and website title.
- The config.json in the production directory includes configuration to purge unused TailwindCSS classes.

#### module.json

- Edit `config/_default/module.json`.
- Include any additional modules you wish to import.
- If you would like to use a different theme then include a reference in this file.

#### params.json

- Edit `config/_default/params.json`.
- Include values for author, avatar, description, tagline and copyright.
- Include any other parameters you would like to use in your templates.
- The debug attribute when set to true will display a banner with the current screen size. This is useful for working with TailwindCSS.
- The js attribute contains configuration for the ESBuild, which is used to build the JavaScript elements of the site.
- The js.app attribute allows you to pass custom parameters into JavaScript libraries that you create.

#### markup.json

- Edit `config/_default/markup.json`.
- Update this file to configure syntax highlighting.

#### menu.json

- Edit `config/_default/markup.json`.
- Update this file to configure the global navigation you would like to use for your site.

### Scripts

- Two NPM scripts are configured in the `package.hugo.json`.
- `build` builds the production site.
- `hugo-server` runs the development site locally.
- Add any other scripts you would like to merge with the project's `package.json` once it is generated.

### Initialise the project

- Initialise the project as a Hugo module.
- If an error occurs then please check this workaround as at the time of writing a bug exists which may impact the import of modules [Workaround](https://discourse.gohugo.io/t/hugo-latest-version-cant-support-server-command-under-examplesite-subfolder/34506/2)

```
% hugo mod init github.com/<github-user>/<website-name>
```

- Pull any submodules into the project (such as the theme).

```
% hugo mod get -u
```

- Create a package.json using the Hugo module npm command.

```
% hugo mod npm pack
```

- Run npm to install the dependencies.

```
% npm install
```

- Make the content, layouts and data directories.

```
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

- Create your own custom templates in the layouts directory to override the theme.
- Add your own modules (such as JavaScript libraries).
- Create a home page (use the theme's block paradigm to add widgets).
- Override the default 404 page.
- Override the default robots.txt.


