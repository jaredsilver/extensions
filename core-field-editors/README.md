Contentful Core Field Editors
=============================

This folder contains the source code for field editors builtin within the
Contentful Web Application. Since these are developed using the
[UI Extensions SDK][ui-extensions-sdk], this will allow you to understand how
each component works, and create your own extensions based on existing
Contentful components' source rather than starting from scratch.

To do this, you should first clone the repository and install the field editor
dependencies as follows:
~~~
git clone https://github.com/contentful/extensions.git contentful-extensions
cd contentful-extensions/core-field-editors
npm install
npm install -g contentful-extension-cli
~~~

Then go to the field editor folder and create a bundle called `editor.dist.html`,
which will be used as the extension's source:
~~~
cd src/textarea
../../bin/bundle
~~~

Finally, create the extension from the `extension.json` definition and the HTML
file.
~~~
export CONTENTFUL_MANAGEMENT_ACCESS_TOKEN=<MY_TOKEN>
contentful-extension create --space-id <MY_SPACE_ID>
~~~

You can now use the component by following the same steps as with any other
[UI extension](https://www.contentful.com/blog/2016/07/06/ui-extensions-sdk/).

[ui-extensions-sdk]: https://github.com/contentful/ui-extensions-sdk