---
title: "Responsive Web Design"
description: "With the advent of smartphones and tablets the number of people using a desktop for their daily internet use has significantly gone down…"
date: "2020-02-07T04:12:00.138Z"
categories: []
published: true
canonical_link: https://medium.com/@rishabhcodes/responsive-web-design-132132df8243
redirect_from:
  - /responsive-web-design-132132df8243
---

With the advent of smartphones and tablets the number of people using a smartphone instead of their personal computers for their daily internet use has increased exponentially. Smartphones have also made the internet more accessible to people. Which in turn means that websites need to be compatible with different devices and screen resolutions to provide a seamless experience to the user to enhance the user experience.

Screen sizes and resolutions play an important role in how websites are rendered by a browser and a website might behave or appear different on different devices. To overcome this developers came up with an approach to maintain a separate website each for desktops as well as for mobile. But this approach is somewhat inefficient since it requires more effort and storage to maintain two separate websites.

![](./asset-1.jpeg)

Lately this approach has been replaced by Responsive Web Design. Responsive web design term was coined and developed by Ethan Marcotte. It is the approach that suggests that design and development should respond to the user’s behavior and environment based on screen size, platform and orientation. The practice consists of a mix of flexible grids and layouts, images and an intelligent use of CSS media queries. As the user switches from their laptop to iPad, the website should automatically switch to accommodate for resolution, image size and scripting abilities.

We shall briefly discuss about how a website is made responsive and about various CSS properties that are used for the same.

Responsive Web Design can be broken down into three main components, including `_flexible layouts_`, `_media queries_` and `_flexible media_`.

### **Flexible Layouts**

Flexible layouts, or the flexible grid system is the practice of building the layout of a website capable of dynamically resizing to any width. It is done using relative length units like `percentages or em units` rather than fixed length units like `px or inches.` These relative units are used to declare common values like the width, margin or padding.

As the size of browser window is changed flexible layouts make it easier for the webpage to adapt and respond to the new size. This takes away the need to maintain a separate website for mobile platforms since the same website can now we used on all platforms.

But how do we make the elements of a webpage respond to this change. That’s where the second component of responsive web design comes in.

### **Media Queries**

The idea of creating a specific stylesheet to come into play under certain conditions . Media queries helps developers to write CSS specifically for certain situations. For example, detecting the user has a small device like a smart phone of some description and giving them a specific layout. Let us suppose there is a section of the web page with a three column layout. To make it easier on the mobile it would be better to linearize the layout, making it all single column. Various sections of the webpage might need to be resized as well to make it more platform independent.

The first way to use media queries is to have the alternate section of CSS right inside your single stylesheet. So to target small devices we can use the following syntax:

```
@media only screen and (max-device-width: 480px) {    
}
```

Here we can add an alternate CSS for devices with screen size equal to or less then 480px or whatever size declared inside the media query. Browsers will automatically detect the screen resolution CSS written specifically for the device resolution will be implemented. By using the cascade we can simply overwrite any styles rules we set for desktop browsers earlier in our CSS. As long as this section comes last in your CSS it will overwrite the previous rules.

### **Flexible media**

As the dimensions of browser window changes the dimensions of media doesn’t. This can cause disproportionate looking webpage and media on the web page. Hence images, videos and other media need to be scalable and their dimensions should change in proportion to the change in browser window dimensions.

Media can be made scalable using the max-width and min-width property in CSS. This property however doesn’t work for embedded media. For embedded media such as Youtube videos which are embedded within `<iframes>` tag in the HTML document the absolute position property in CSS is used. The embedded elements need to have a width of 100% so that it’s dimensions vary based on the change in dimensions of viewport or the screen resolution.
