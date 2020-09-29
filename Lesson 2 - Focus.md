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

Tab order is generally determined by DOM order, meaning you should take care when styling may cause the rendered position to not corrolate to the position in the DOM. It can also manually specified using the `tabindex` HTML attribute.