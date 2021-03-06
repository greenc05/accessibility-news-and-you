---
layout: page
title: Accessibility, News and Testers
---
Accessibility testing should be done as part of the **Definition of Done**.

## Checklist - Automated

0. Check code for errors against **BBC Accessibility Standards**, either by using [bbc-a11y](https://github.com/bbc/bbc-a11y) in the terminal or by using the bbc-a11y Pa11y Dashboard (Dashboard to be released early 2017).

0. Automated testing with SHIVE (HIVE for Screen Readers) - Have **cucumber tests** been written against the accessibility acceptance criteria? Do they pass? Note, SHIVE is not yet in production, however the tests should still be written so we are ready to go when it is.

0. Have **End to End Tests** been written to cover accessibility? Do they pass? A tool such as [Axe](https://www.deque.com/products/axe/), can be integrated, for example if using React, via [React Axe](https://github.com/dylanb/react-axe) or the [bbc-a11y](https://github.com/bbc/bbc-a11y) CLI could be used.

## Checklist - Manual

0. **Design** - Are elements styled correctly? e.g. Do links use the standard link colour and have the standard associated hover and focus styles?

0. Do all elements meet [**colour contrast**](http://www.bbc.co.uk/guidelines/futuremedia/accessibility/mobile/design/colour-contrast) levels? Use a tool such as [contrast checker](http://webaim.org/resources/contrastchecker/) to check. All colours should meet a level of 4.5:1 or higher.

0. **Colour blindness** - Use the [ChromeLens](http://chromelens.xyz/) dev tool extension to view the code with different vision issues.

0. Does the design use **icons**? Meaning should not just be conveyed with icons/images, do the icons have off-screen (visually hidden) text so users of assistive technology don't miss out? Check by inspecting the element in the web browser or with a screen reader.

0. **Manually check the heading order**. Do the headings and the heading order actually make sense? If working on a **foreign language site**, use Google Translate to check what the headers actually say. You can use a tool such as the [Web Developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) add-on for Chrome or Firefox. (Under ‘Information’ select ‘View Document Outline’ - This will show you the heading structure for the selected page.)

0. **Check the accessibility of the rendered DOM**. Use a tool such as the [Axe browser extension](https://www.deque.com/products/axe/#aXeExtensions).

0. **Keyboard navigation**
  0. Check the **tab order is correct** when using the keyboard and the tab key. Can you see where you are on the page at all times e.g. Is there focus styling? This should be the same as the hover styles.

  0. Is the **keyboard focus** always in the correct place? e.g. After selecting a 'More' button with the return key you should be taken to the new content displayed with the next press of the tab key.
  0. When using '**Trace tab path**', the path should go from left to right as you work your way down the page (there will be some exceptions to this order, such as when the 'Breaking news' banner is on the page). Use the [ChromeLens](http://chromelens.xyz/) dev tool extension to trace the tab path.

0. **Has the feature been considered without javascript**? It should degrade gracefully. Use a tool such as the [Web Developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) add-on for Chrome or Firefox to easily turn Javascript off.

## Checklist - Assistive Technology

Test with [Supported Assistive Technology](accessibility-and-supported-assistive-technology), using an actual device if possible.

0. Is the feature useable?
0. Does the feature make sense?

### Checklists for other roles in the team

- [Product Owner](accessibility-news-and-product-owners)
- [Designer](accessibility-news-and-designers)
- [Business Analyst](accessibility-news-and-business-analysts)
- [Developer](accessibility-news-and-developers)
