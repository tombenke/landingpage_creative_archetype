landingpage_creative_archetype
==============================

This is [kickoff](http://tombenke.github.io/kickoff/) project archetype for landing page creation.
It is based on the [Creative](http://startbootstrap.com/template-overviews/creative/)
one page Bootstrap theme for creative portfolios and businesses.

## Usage

### Prerequisites

You must have [Node.js](https://nodejs.org/en/) and the [kickoff](http://tombenke.github.io/kickoff/) utility installed.

### Create a new project

You can create a new project with the following command:

    kickoff -f tombenke/landingpage_creative_archetype -d new_project_name

The utility will download the project template from GitHub, then asks some qouestions,
that you may give, or simple press `Enter` in case you are satisfied with the default answers.

    You are generating a single page website using the startbootstrap-creative template.

    ? The name of the project: mysite
    ? The short description of the project: This is my single page website.
    ? The contact email address: contact@mydomain.com
    ? The contact phone number: (+??) ?????-???
    ? The full name of the author: Anonymous
    ? The email address of the author: anonymous@some-domain.com
    ? The github account (username) of the author: anonymous
    ? The title of the page: My Site
    ? The Home Heading text: The Home-Heading above the UVP
    ? The Unique Value Proposition: This is the UVP, you can define it later
    Converting package.json as Handlebars template
    Converting src/parameters.json as Handlebars template

After all the questions answered, the project will be generated.
The project has the following structure:

├── dist
└── src
    ├── css
    ├── img
    │   └── portfolio
    ├── js
    ├── less
    ├── md
    ├── partials
    └── templates

The `src` folder contains the source files.
The additional vendor files will be copied from the corresponding node modules after installation.
The results will arrive into the `dist` folder.

The `src/templates` folder contains [`mustache`](https://www.npmjs.com/package/mustache) templates,
that may include files from the `src/partials` folder.
The `src/md` folder may contain [`markdown`](https://www.npmjs.com/package/markdown) format files,
that will be converted to HTML format and will be placed into the `partials` folder
so page templates can be written to envelop these contents.

The `src/img` folder contains the sample images, that you should replace with your own photos.
The `src/less` folder contains the [`less`](http://lesscss.org/) files, that you may customize.
Especially the is important, [`src/less/variables.less`](src/less/variables.less) which contains the most relevant syling parameters.

You can do the following steps:

1. Install the npm modules required by the newly generated application:

       cd new_project_name
       npm install

2. Edit the template and the parameter files according to your needs:

    - src/templates/index.html
    - src/parameters.json

3. Change the images under the `src/img` folder.
4. To create the dist package, run either:

       npm run build

   or

       npm run watch

The build process happens via the gulp utility. If you change the project structure, you may also modify the [gulpfile.js](gulpfile.js) as well.
The `npm run watch` uses the [browser-sync](https://www.browsersync.io/) utility, that starts a server too.
With this command, you can immediately view the results in a browser, that will be automatically refreshed,
in case you modify any of the source content, can be found under the [`src`](src/) directory.

The final results will be written into the `dist` folder.
You can copy the whole content to the final place of deployment when you are ready.

## References
- [Creative](http://startbootstrap.com/template-overviews/creative/)
- [browser-sync](https://www.browsersync.io/)
- [gulp-markdown](https://github.com/sindresorhus/gulp-markdown)
- [gulp-mustache](https://github.com/sindresorhus/gulp-markdown)
- [mustache](https://www.npmjs.com/package/mustache)
- [markdown](https://www.npmjs.com/package/markdown)
- [The less CSS pre-processor](http://lesscss.org/)
- [kickoff](http://tombenke.github.io/kickoff/)

