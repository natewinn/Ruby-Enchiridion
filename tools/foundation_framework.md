Foundation Framework
====================

# What is Foundation?
[Foundation](http://foundation.zurb.com/index.html) is a [responsive](http://en.wikipedia.org/wiki/Responsive_Web_Design) framework originally created by [Zurb](http://zurb.com/) as a template for their in-house projects. It's labeled as "the most advanced responsive front-end framework in the world." The project was open sourced by Zurb in October 2011 and has since encouraged developers to make their own [contributions](https://github.com/zurb/foundation). Zurb has a [great write-up](http://zurb.com/word/framework) that explains why they created Foundation and the purpose of using a framework. 

Foundation is comprised of HTML and CSS-based design and draws on an extensive use of Javascript. This includes typography, forms, buttons, navigation, and [many interface elements](http://foundation.zurb.com/docs/components/kitchen_sink.html). Some [big names sites](http://zurb.com/responsive?utf8=%E2%9C%93&style_id=&framework_id=1&name_or_style=), including [Dictionary.com](http://dictionary.com/), use it. Though Foundation lacks style out of the box, its name promises exactly what it provides . . .an unopinionated "foundation" for your design. With an extensive user community and almost daily commits, Foundation is a framework you can rely on.
	
# How can I get started?
 Getting started with Foundation is fast and easy. There are two ways to get Foundation up and running on your Rails app . . .
 
### Add the Rails Gem

1. Add the [Foundation gem](https://github.com/zurb/foundation-rails) to your `Gemfile`
		
        gem 'foundation-rails'
		
2. Run `bundle install` in the terminal
3. Run this command in terminal

        rails g foundation:install

### Manually Install

1. [Download](http://foundation.zurb.com/develop/download.html) Foundation files

2. Include the `foundation.css` file in the `app/assets/stylesheets` directory

3. Append the following text to the `app/assets/stylesheets/application.css` file
		
        *= require_foundation

# How do I use it?
A good place to get started are the [Foundation docs](http://foundation.zurb.com/docs/). Another fantastic resource to check out is [Foundation and Rails](http://railsapps.github.io/rails-foundation.html) by Daniel Kehoe. After looking over the docs, you'll notice the three major parts of Foundation:

## 1. The Grid
If you're not familiar with a grid system, it's comprised of CSS classes that utilize common dimensions in a column-based format. This greatly decreases layout time and markup. Another benefit of using a grid is allowing the design to be scaled without altering its original form. The Foundation grid system is made up of a 12 column "container" that allows other columns to be nested within it. This [example](http://foundation.zurb.com/templates/banded.html) is a great reference. After following the link, right-click on the page and select "view source" to see how the grid is setup.

You can always take a peek at the Foundation [grid docs](http://foundation.zurb.com/docs/components/grid.html) to get going, but the [Beginner's Guide to Foundation Grids](http://blog.teamtreehouse.com/beginners-guide-grids-zurb-foundation-5) might be a better place go if you're just getting started. 

You'll find 5 classes to be used with the grid—`row`, `columns`, `small-#`, `medium-#`, and `large-#`. The three "size" classes are to designate layout for mobile, tablet, and desktop/laptop respectively. If all size classes are not notated, the styling of the smaller class that is notated will be inherited by the "larger"" class. Though not included, the `large-#` class would inherit 8 columns from `medium-8`.

    .small-6.medium-8.columns

Some other useful features that are baked into Foundation's grid system are nest, center, offset, and incomplete rows. Check out the [grid docs](http://foundation.zurb.com/docs/components/grid.html) for additional details.

## 2. The Elements
A go-to reference for every Foundation element is the [Kitchen Sink](http://foundation.zurb.com/docs/components/kitchen_sink.html). Here you'll find every included Foundation element at a glance. To drill down into further detail regarding a specific element, reference the left navigation bar on the [Kitchen Sink](http://foundation.zurb.com/docs/components/kitchen_sink.html) page. Each link provides a dedicated page that will open to further explain the element(e.g. [Buttons](http://foundation.zurb.com/docs/components/buttons.html)). This page includes a description, element variations, possible use cases, and code snippets. For example, all of the available button appearances as seen below can be found there:

     / Size Classes
     %a.button.tiny{href: "#"} Tiny Button
     %a.button.small{href: "#"} Small Button
     %a.button{href: "#"} Default Button
     %a.button.large{href: "#"} Large Button
     
     / Color Classes
     %a.button.success{href: "#"} Green Button
     %a.button.alert{href: "#"} Red Button
     %a.button.secondary{href: "#"} Alternate Button
     
     / Radius Classes
     %a.button{href: "#"} Regular Button
     %a.button.radius{href: "#"} Radius Button
     %a.button.round{href: "#"} Round Button
     
     / Disabled Class
     %a.button.disabled{href: "#"} Disabled Button
     
     / Expand Class
     %a.button.expand{href: "#"} Expanded Button

## 3. The Extras
The "extras" include all the nifty JavaScript magic available in Foundation. Again, you can reference the [docs](http://foundation.zurb.com/docs/javascript.html) to get rolling. In the previously mentioned [Kitchen Sink](http://foundation.zurb.com/docs/components/kitchen_sink.html) left-nav bar, the elements listed that utilize JavaScript will be notated with a `JS` symbol next to the corresponding link. If the `rails g foundation:install` command was used when configuring Foundation, you're all set. If not, include the `foundation.js` file from the Foundation download in the `app/assets/javascripts` directory and append the text below to the `app/assets/stylesheets/application.js` file:

     //= foundation

By simply including `foundation.js` in the asset pipeline, you will have the necessary files to access all of Foundation's JavaScript elements. Each JavaScript element will have a dedicated page include the same info as the standard element pages (i.e.  description, element variations, possible cases, and code snippets), but will also include additional configuration instructions. 

## Where Do I Go From Here?
If you're just getting started, the docs can be a bit overwhelming. Here are a few video tutorials to check out so you can hit the ground running . . .

1. [How to Get Started with Foundation 5](http://www.webdesignerdepot.com/2013/11/how-to-get-started-with-foundation-5/) includes a short video that demonstrates the initial setup in under 20 minutes.

2. [RailsCast on Foundation](http://railscasts.com/episodes/417-foundation) covers Foundation 4 (which is not the latest version), but will still provide some helpful insights on integrating Foundation into your Rails app.

3. [Beginner's Guide to Foundation Grids](http://blog.teamtreehouse.com/beginners-guide-grids-zurb-foundation-5) and [Foundation and Rails](http://railsapps.github.io/rails-foundation.html) as previously mentioned are also must reads when getting started with Foundation.

## Helpful tips for using Foundation
1. **What's the deal with the `.min` CSS and JavaScript files?** These are "minified" files that are much smaller in size. However, if you want to pick apart the CSS (and of course you do), include the "regular" CSS file.
2. **Not sure what to do with the blank slate?** Here are some great [starter templates](http://foundation.zurb.com/templates.html) created by Zurb to get started on the right foot.
3. **Are you having an issue with Foundation and not sure what to do?** Zurb created [this page](http://foundation.zurb.com/support/support.html) to show all the possible ways to find help with Foundation.
4. **Don't need everything foundation has to offer?** Head on over to the Foundation [download page](http://foundation.zurb.com/develop/download.html) and you will find a buffet-style Customize Foundation feature to download Foundation with *just* the features you need.
5. Sick of taking the time to adjusting your css to center elements in a `div`? Use the `small-centered`, `medium-centered`, or `large-centered` to automagically center columns on the page. You can even even selectively uncenter a column like in the example below.

        .small-9.small-centered.large-uncentered.columns

Forum | GitHub | Twitter
--- | --- | --- 
[Foundation Forum](http://foundation.zurb.com/forum) | [GitHub Repo](https://github.com/zurb/foundation) | [Twitter Account](https://twitter.com/ZURBfoundation)