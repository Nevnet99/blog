---
title: 'WCAG 2.2 - What You Need to Know'
description: 'A summary of the new WCAG 2.2 guidelines updates'
pubDate: 'Oct 7 2023'
heroImage: '/codecult-placeholder.png'
---

## Table of contents
- [What is WCAG?](#what-is-wcag)
- [What's new in WCAG 2.2?](#whats-new-in-wcag-22)
  - [2.4.11 Focus Not Obscured (Minimum) (AA)](#2411-focus-not-obscured-minimum-aa)
  - [2.4.12 Focus Not Obscured (Enhanced) (AAA)](#2412-focus-not-obscured-enhanced-aaa)
  - [2.4.13 Focus Appearance (AAA)](#2413-focus-appearance-aaa)
  - [2.5.7 Dragging movements (AA)](#257-dragging-movements-aa)
  - [2.5.8 Target Size (Minimum) (AA)](#258-target-size-minimum-aa)
  - [3.2.6 Consistent Help (A)](#326-consistent-help-a)
  - [3.3.7 Redundant Entry (A)](#337-redundant-entry-a)
  - [3.3.8 Accessible Authentication (Minimum) (AA)](#338-accessible-authentication-minimum-aa)
  - [3.3.9 Accessible Authentication (Enhanced) (AAA)](#339-accessible-authentication-enhanced-aaa)
  
<br />

---

<br />

### What is WCAG?

WCAG stands for Web Content Accessibility Guidelines. It is a set of guidelines that help make web content more accessible to people with disabilities. The guidelines are organized into three levels of conformance: A, AA, and AAA. The WCAG 2.2 guidelines are an extension of the WCAG 2.1 guidelines and have recently (Oct 6 been released!).

### What's new in WCAG 2.2?

You can check out the change list of WCAG 2.2 guidelines <a href="https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/" target="_blank">here</a>. The following is a summary of the new guidelines:

- 2.4.11 Focus Not Obscured (Minimum) (AA) | Partially visible focus rings
- 2.4.12 Focus Not Obscured (Enhanced) (AAA) | Ensure when an item gets keyboard focus, it is fully visible.
- 2.4.13 Focus Appearance (AAA) | Use a focus indicator of sufficient size and contrast.
- 2.5.7 Dragging movements (AA) | For any action that involves dragging, provide a simple pointer alternative 
- 2.5.8 Target Size (Minimum) (AA) | For any touch point now the minimum must be 24x24 px
- 3.2.6 Consistent Help (A) | Put help links in consistent places across webpages 
- 3.3.7 Redundant Entry (A) | Don't ask for the same information twice in the same session (for example: asking for the users email again at the end of a form although the first step was to enter their email)
- 🚨 3.3.8 Accessible Authentication (Minimum) (AA) | Don't make people solve, recall, or transcribe something to login (Captchas are now no good in terms of accessibility)
- 🚨 3.3.9 Accessible Authentication (Enhanced) (AAA) | Same as above but don't use images (click the squares with cars)

lets jump into each of these new guidelines and see what they mean.

---

<br />

#### 2.4.11 Focus Not Obscured (Minimum) (AA)

This guideline is about making sure that when an item gets keyboard focus, it is fully visible. This is important because if a user is navigating your site with a keyboard, they need to be able to see where they are on the page. If the focus ring is not visible, they will not know where they are on the page.

#### 2.4.12 Focus Not Obscured (Enhanced) (AAA)

This guideline is similar to the previous one, but it is more strict. It requires that the focus ring is fully visible, not just partially visible.

#### 2.4.13 Focus Appearance (AAA) 

This guideline is about making sure that the focus ring is visible enough. It requires that the focus ring has a contrast ratio of at least 3:1 with the background color of the element it is on. It also requires that the focus ring is at least 2 CSS pixels wide.

#### 2.5.7 Dragging movements (AA) 

This guideline is about making sure that any action that involves dragging has a simple pointer alternative. This is important because if a user is navigating your site with a keyboard, they need to be able to perform the same actions as someone who is using a mouse. If there is no simple pointer alternative, they will not be able to perform the action.

#### 2.5.8 Target Size (Minimum) (AA) 

This guideline is about making sure that any touch point is at least 24x24 px. This is important because if a user is navigating your site with a touch screen, they need to be able to tap on the touch point. If the touch point is smaller than 24x24 px, they will not be able to tap on it.

#### 3.2.6 Consistent Help (A) 

This guideline is about making sure that help links are in consistent places across webpages. This is important because if a user is navigating your site with a keyboard, they need to be able to find the help link. If the help link is not in a consistent place, they will not be able to find it. A good example of a persona that would benefit from this guideline is someone who is has cognitive issues relating to memory.

#### 3.3.7 Redundant Entry (A) 

This guideline is about making sure that you don't ask for the same information twice in the same session. This can be confusing for some users if they have already entered the information once. 

#### 3.3.8 Accessible Authentication (Minimum) (AA)

This guideline is about making sure that you don't make people solve, recall, or transcribe something to login. This in my opinion is the most interesting as it means that Captchas are no longer accessible. Adding to this, the proposed solution for authentication is to use a magic link. This is a link that is sent to the users email and when they click on it, they are logged in.

#### 3.3.9 Accessible Authentication (Enhanced) (AAA)

This guideline is similar to the previous one, but it is more strict. It requires that you don't use images for authentication. This means that you can't use a Captcha that asks the user to click on the squares with cars in them. To my knowledge to be AAA accessible you would need to use a magic link for all authentication.


#### ⭐️ Extras 

Thanks for reading to the end below are some extra resources that you might find useful:

- Deque dev tools (great tool to run a accessibility audit on your site): <a href="https://www.deque.com/axe/devtools/" target="_blank">here</a>
- Color contrast checker: <a href="https://webaim.org/resources/contrastchecker/" target="_blank">here</a>
- WCAG 2.2 guidelines: <a href="https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/" target="_blank">here</a>