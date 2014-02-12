The `gh-pages` branch contains generated demo pages for http://angular-ui.github.com/bootstrap as well as build results.

#安装

所有在这个库中的指令只依赖AngularJS和bootstrap的CSS。没有必要引入任何第三方JavaScript文件。

bootstrap CSS可以从CDN中引用: http://www.bootstrapcdn.com/

Then it is enough to include one of the build files described below.

##构建

在这个仓库可以发现具有以下名称的构建文件:

* ui-bootstrap-[version].js
* ui-bootstrap-tpls-[version].js
* ui-bootstrap-[version].min.js
* ui-bootstrap-tpls-[version].min.js

Files with the `min` suffix are minified versions to be used in production.

Then we've got files with the `-tpls`. To explain the difference let's start by explaining that we want our directives to be highly customizable. To achieve this we are trying hard not to hard-code markup nor CSS inside JavaScript code. Instead most of the directives are coming with a dedicated template(s) so people can change them. We are providing default templates based on Twitter's markup and CSS but you should be able to prepare your own partials to change the look&feel of widgets from this repo.

Now it should be clear that files with the `-tpls` in their name have bootstrap-specific templates bundled with directives. For people who want to take all the directives and don't need to customize anything the solution is to grab a file named `ui-bootstrap-tpls-[version].min.js`. If, on the other hand default templates are not what you need you could take `ui-bootstrap-[version].min.js` and provide your own templates, taking the default ones (https://github.com/angular-ui/bootstrap/tree/master/template) as a starting point.
