# Frontend Foundation

### Table of Contents

* [Web Accessibility](#web-accessibility)
* [Mobile-first Design](#mobile-first-design)
* [HTML](#html)
  * [a Link Tags and Referrer Attacks](#a-link-tags-and-referrer-attacks)
* [CSS](#css)
  * [CSS Grid](#css-grid)
  * [Flexbox](#flexbox)
  * [CSS Animation](#css-animation)
  * [Bootstrap](#bootstrap)
* [SASS](#sass)
* [JS](#js)
  * [JS Animation](#js-animation)
  * [VueJS](#vuejs)
  * [ReactJS](#reactjs)
* [SVG](#svg)

## Web Accessibility

Web Accessibility refers to how accessible the content of a website is to a person with a disability, such as vision impairment, color blindness, hearing impairment, movement restriction, cognitive impairment, et cetera.

Web accessibility is **extremely important** and must be a fundamental consideration for any UI/UX design and development.

Some web accessibility resources:

- [ColorSafe.co - Accessible Color Palette Creation Tool](http://colorsafe.co/)
- [W3C - Introduction to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/)
- [ARIA HTML attributes](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)

## Mobile-first Design

The easiest way to lay out a website UI is to style it **mobile-first** -- this means writing styles for how columns/rows should look on the smallest possible screens (extra-small, or xs), then laying down styles/columns for small (sm), medium (md), large (lg), and extra-large (xl) screens after you establish xs screen styles.

In most cases, your columns on xs screen sizes should be full-width (as in single-column rows).

Responsive web design is easily achieved using [CSS Grid](#css-grid) or [Flexbox](#flexbox), or a CSS library that implements pre-written responsive css grid/flexbox layout classes, such as Bootstrap, SemanticUI, MaterialUI, and others.

An example of Bootstrap grid classes for two-column layouts:

```html
<div class="container">
  <div class="row">
    <div class="col-12 col-md-6">
      Column One
    </div>

    <div class="col-12 col-md-6">
      Column Two
    </div>
  </div>
</div>
```

## HTML
#### Hyper-Text Markup Language

### a Link Tags and Referrer Attacks

The beloved `<a>` tag: it acts as our window to the world outside our webpage -- but sometimes it can act as a window into our web page from the target we are linking to.

Whenever we code an `<a>` tag to open its `href` in a new tab, e.g.: `<a href="https://google.com" target="_blank">...</a>`, it gives the web page we are linking to (`"https://google.com"` in this case) the ability to redirect, read, and manipulate our page's window.

For instance, if we link to a malicious site with `target="_blank"` without appropriate safeguards, that malicious site may redirect the origin window (our page where the `target="_blank"` link exists) to a fake Facebook login, or fake bank account login, as an attempt to steal our user's login credentials or personal information.

All is not lost, however; we can safeguard against this attack with the `rel=""` HTML attribute like so:

```html
<a href="https://google.com" target="_blank" rel="noopener noreferrer">This link opens in a new tab.</a>
```

Adding `rel="noopener noreferrer"` removes all information about the referring webpage (our webpage with the above `<a>` link) from the new tab HTTP `GET` request headers for the `<a>` link's target URL.

For additional information about this exploit and these `<a>` tag attributes, check out the links below:

* [Target="_blank" - the most underestimated vulnerability ever](https://www.jitbit.com/alexblog/256-targetblank---the-most-underestimated-vulnerability-ever/)
* [What You Need to Know about rel="noreferrer" Attribute](https://www.techwyse.com/blog/search-engine-optimization/what-you-need-to-know-about-rel-noreferrer-attribute/)
* [The Difference Between nofollow and noreferrer](https://www.forbes.com/forbes/welcome/?toURL=https://www.forbes.com/sites/johnrampton/2017/11/06/the-difference-between-nofollow-and-noreferrer-and-why-it-matters/&refURL=https://www.google.com.hk/&referrer=https://www.google.com.hk/)
* [Exploiting Referrer Headers](https://www.gremwell.com/exploiting_xss_in_referer_header)

## CSS
#### Cascading Style Sheets

coming soon: Classes, IDs, Animations,

### CSS Grid

### Flexbox

### CSS Animation

### Bootstrap

Bootstrap is a great CSS library for putting together responsive frameworks very quickly.

You may have worked with Bootstrap before, but if you have only worked with Bootstrap versions older than 4.0, some key class names have changed. [Click here for info on the changes from Bootstrap <4 to Bootstrap 4.](https://getbootstrap.com/docs/4.0/migration/)

Another nice thing about Bootstrap 4: official SASS theming and variables :D

* [Official Bootstrap 4 Docs](http://getbootstrap.com/docs/4.1/getting-started/introduction/)
* [Bootstrap SASS Theming](https://getbootstrap.com/docs/4.0/getting-started/theming/)

#### Bootstrap JS

For regular HTML/CSS, Bootstrap has optional JQuery-dependent JS dependencies that make its modals and animations work.

If you are working in a JSS -> HTML library/framework such as VueJS or ReactJS, create those animations/behaviors with state-dependent functions rather than JQuery or Bootstrap.js (or search the Internet for VueJS/ReactJS implementations of Bootstrap)

For **Vue** projects, [Bootstrap-Vue](https://bootstrap-vue.js.org/docs/) is a phenomenal Bootstrap 4 component library that implements VueJS functionality rather than JQuery-based Bootstrap.js.

## SASS

coming soon: sass variables, theming, and building sass

* [Official SASS Guide](https://sass-lang.com/guide)

## JS
#### JavaScript

coming soon

### JS Animation

* [GreenSock](https://greensock.com/)
* [Velocity](http://velocityjs.org/)
* [Anime](http://animejs.com/)

todo: add content + the comparison slides from val head's webconf.asia presentation

### VueJS

### ReactJS

## SVG
