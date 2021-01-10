# Lesson 2: Focus

## Introduction to Focus
In a nutshell, focus determines where events from the keyboard or other input device are sent to on the page.

For most users this is achieved by selecting an element by clicking on it, or by using `Tab` key shortcuts  to cycle through elements.

The currently focused item is often indicated by a stylised focus ring.

## Importance of Focus
For users that primarily drive their computers with the keyboard or other input device focus is absolutely critical - it is their primary means of accessing everything. Web AIM checklist states in section 2.1.1 that all page functionality should be available using the keyboard.

Certain users also just prefer to navigate using solely the keyboard, meaning a well-implemented focus strategy means a better experience for everyone.

## Tab Order
Tab order describes the order in which elements are cycled through when using the `Tab` and `Shift` + `Tab` keyboard shortcuts. Ensuring your application has a logical tab order is an important step.

Built-in interactive HTML elements such as input fields, buttons, and dropdown selections are **implicitly focusable**. This means they are automatically inserted in the tab order.

Non-interaction elements such as titles, paragraphs, and images are not implicitly focusable and therefore aren't automatically included in the tab order.

Tab order is generally determined by DOM order, meaning you should take care when styling may cause the rendered position to not correlate to the position in the DOM. It can also be manually specified using the `tabindex` HTML attribute, however this should only be used for interactive elements.

## Managing Focus
Managing focus involves keeping the user's interactive context in sync with the visual representation of the site.

An example of where this would be important is a single-page web app where navigation changes the page's content. In order to focus these sections, he can ensure their headers are able to be programmatically focused by setting their `tabIndex` to `-1`:

```
<h2 tabindex=-1>What is Vegemite?</h2>
```

Now we have set the `tabIndex`, we can now focus the section's header in our navigation code:

```
 newPage.querySelector('h2').focus();
```

### Skip Links
On most websites the main content is usually not the first thing in the DOM, instead often beginning with navigation links, side bars, hamburger menus, etc. This means some users must navigate through a lot of content before reaching the main purpose of the page.

This can be solved by including a 'Skip Link' that allows users to skip directly to the main page content. This link will be placed early in the DOM so it can be immediately accessed.

### Custom Components
Sometimes focus will need to be managed at the component level as well. Native HTML elements have certain expected focus-related keyboard behaviours, and if we are making custom components it is expected that these keyboard behaviours also exist.

The [ARIA Authoring Practices](https://www.w3.org/TR/wai-aria-practices/) doc lists the various keyboard interactions that are supported by different components, and acts as an excellent resource when adding behaviour to custom components.

## Offscreen Content
With certain component design patterns, such as sidebars that are toggleable with a menu icon, it is possible to be in a situation where focusable elements are not currently visible on the screen. This isn't ideal, as it leads to the interaction context being out of sync with the visual representation.

One way of diagnosing such issues is using the Chrome [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb?hl=en) extension. It provides a number of useful features, including a set of accessibility audits that can diagnose issues such as hidden elements.

## Keyboard Traps
A keyboard trap describes a situation where focus is locked or trapped at one particular page element.

An example of this would be an input field which uses `Tab` to confirm auto-complete, meaning users cannot cycle to the next element of the tab cycle.

However, there may be instances where we want to temporarily trap the focus within a certain area, such as when displaying modal. 
