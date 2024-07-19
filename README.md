<div align="center">
  <h1 align="center">Scroll-Animation</h1>  
    <img src="images/video.gif" alt="Scroll-Animation" />  
</div>

## Overview

In web design, scroll animations refer to animations triggered as a user scrolls down or up a webpage. These animations can include elements fading in, sliding into view, or changing size or position in response to the user's scrolling behavior. They are often used to enhance user experience by making the website more dynamic and engaging.


## Table of Contents

- [Overview](#overview)
- [Animation-timeline in CSS](#animation-timeline-in-css)
- [View() in CSS](#view-in-css)
- [Implementation](#implementation)
- [Live Demo](#live-demo)
- [Conclusion](#conclusion)


## Animation-timeline in CSS

In CSS, the `animation-timeline` property is used to create scroll-based animations. It allows you to connect an element, called the "subject," to a view progress timeline. This timeline tracks how much of the subject is visible within its nearest scrollable container.

There are two main types of view progress timelines:

### Anonymous View Progress Timeline

This timeline is created directly on the subject element itself by setting `animation-timeline: view()`. You can specify the scroll axis (vertical or horizontal) to track progress and a padding value to adjust the area considered "in view" for the subject.

### Named View Progress Timeline

This involves explicitly naming the timeline using the `view-timeline-name` property (or the shorthand `view-timeline`) on an element. Then, you link the element you want to animate by setting its `animation-timeline` property to the name you created.

Essentially, `animation-timeline` lets you control how an animation progresses based on how much of the element is scrolled into view.

## View() in CSS

The `view()` function in CSS `animation-timeline` defines an anonymous view progress timeline. This timeline determines how an animation progresses based on the visibility of an element (the subject) relative to its nearest scrollable container.

Here's a breakdown of how it works:

- **Subject Element:** You apply the `animation-timeline: view(parameters);` property to the element whose animation you want to control based on scrolling. This element is called the subject.
- **Parameters:**
  - **Axis (x or y):** This specifies the scroll axis (horizontal or vertical) that will be tracked to determine the animation progress. By default, it's vertical (y).
  - **Padding Value:** This value defines a padding area around the viewport. The element is considered "in view" only if part of it lies within this padded viewport area. A padding of 0px means the entire element must be visible.
- **Animation Timeline:** The `view()` function creates a timeline based on the subject's visibility within the scroll container. As the element scrolls into view (along the specified axis and considering the padding), the animation progresses accordingly.

## Implementation

Here's a basic example of implementing a scroll animation using CSS only:

### HTML

```html
<div class="scroll-container">
  <div class="scroll-element">Content to animate</div>
</div>
```
## Live Demo

Check out the live demo of the 3D image slider [here](pkulal.github.io/Scroll-Animation/).

## Conclusion

Creating scroll animations using CSS only is an efficient and elegant solution for enhancing web user experience. By leveraging the power of CSS, you can create visually appealing, interactive elements that animate based on scrolling behavior, without relying on JavaScript. This approach ensures better performance, easier maintenance, and improved SEO.

Thank you for visiting my project!

---

*This README was generated with ❤️ by Praneeth Purushothama Kulal*
