## Twitter Bootstrap for Rails 3 简介

Bootstrap 是由 Twitter 设计的用于加速网络应用和网站开发的工具包。包括了排版 (typography)、表单 (forms)、按钮 (buttons)、表格 (tables)、网格 (grids)、导航 (navigation)等基本的CSS和HTML。

其中，anjlab-bootstrap-rails 项目整合了 Bootstrap 的 CSS 样式 (支持SASS) 和 JS 工具包，可以方便地用于 Rails 3 项目。

备注：这个项目基本克隆了Xdite的 [bootstrap-rails](https://github.com/xdite/bootstrap-rails)，为了方便定制和升级，所以克隆，并升级至 Bootstrap 2.0。

## Rails 3 项目使用指南

### 在 Gemfile 文件中包括 Bootstrap for Rails

```ruby
gem 'simple_form', '~> 2.0.1'
gem 'bootstrap-rails', :require => 'bootstrap-rails', :git => 'git://github.com/qingping/hujoy-bootstrap-rails.git'
```

### 然后，运行 `bundle install`

## Stylesheets

在 `app/assets/stylesheets/application.css` 文件中包含必要的样式文件

```css
*= require bootstrap
```

你可以覆盖 Bootstrap 的变量

```scss
// Create app/assets/stylesheets/bootstrap.scss
// CSS Reset
@import "reset.scss";

// Core variables and mixins
@import "variables.scss"; // Modify this for custom colors, font-sizes, etc

$linkColor: red; // Make all links red

@import "mixins.scss";

// Grid system and page structure
@import "scaffolding.scss";

// Styled patterns and elements
@import "type.scss";
@import "forms.scss";
@import "tables.scss";
@import "patterns.scss";
```

## Javascripts

在 `app/assets/javascripts/application.js` 文件中添加必要的 JavaScripts 文件

```javascript
// Include all twitter's javascripts
//= require bootstrap

// Or pick any of them yourself
//= require bootstrap-alerts
//= require bootstrap-dropdown
//= require bootstrap-modal
//= require bootstrap-twipsy
//= require bootstrap-popover
//= require bootstrap-scrollspy
//= require bootstrap-tabs
```
        
## 鸣谢

Thanks to Twitter for Bootstrap
http://twitter.github.com/bootstrap

Inspired by Xdite and her [bootstrap-rails](https://github.com/xdite/bootstrap-rails)

Also indirectly inspired by Seyhun Akyürek and his [twitter-bootstrap-rails gem](https://github.com/seyhunak/twitter-bootstrap-rails)

## 版权和许可

**Copyright (c) 2011 AnjLab**

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.