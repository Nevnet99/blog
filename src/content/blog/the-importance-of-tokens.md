---
title: 'The importance of design tokens'
description: 'Tokens are a great way to keep your design system consistent and easy to maintain.'
pubDate: 'Sep 28 2023'
heroImage: '/codecult-placeholder.png'
---

## What are Tokens ?

Design tokens are a shareable format between Design, Development and other tooling. They help to keep your brand consistent across all platforms and make it easy to maintain.

A token can be as simple as a HEX value for a color or something more complex like a specific easing function you use for animations or a font size. Realistically a token can be anything you want it to be as long as it's a value you would reuse across your application.

A token abstracts away the value and replaces it with a name, for example instead of using `#000000` for the background of your website, you would use `dark-primary-background`. This makes it easier to change the value of the token without having to change it in multiple places as well as knowing exactly what you will effect, in this case it would be the primary background used in the application for a user that prefers dark mode.

The most important benefit from using tokens is you have a single source of truth for your design system. This means that you can use the same tokens across your entire application and know that they will be consistent, without tokens you would have to remember the values you used for each color, font size, etc. and hope that you don't make a mistake (which is pretty common if you're building a large application).

## When should I implement design tokens ? 

If you're building any application with multiple developers, multiple designers and other stakeholders, you should consider implementing tokens. They will help you keep your design system consistent and easy to maintain, less drift will happen between development and the design and you can keep your brand consistent across all platforms (Design, Application as well as any branding work can use your tokens).

In my personal opinion the size of the application does not matter as in most cases it will scale in size as there is always another thing that needs to be added, so getting tokens in place early will help you in the long run.

## How do I implement tokens ?

There are many ways to implement tokens, to start off with you can use a simple JSON file that contains all your tokens and import it into your application. This is a great way to get started and is easy to maintain, however it does not scale well as you will have to manually update the JSON file and then import it into your application. You can import these into figma via  plugin called TokenOS 

The next step up from this is to use figma variables or Token Studio with Figma to have Figma as your single source of truth for tokens, then using Amazon Style Directory you can generate tokens via whatever format you require CSS, SCSS etc. I would also advice making the repo for tokens separate from your application as it will make it easier to maintain and update, allowing you to version your tokens so that they can be checked before they are merged into your application.

## Conclusion

Tokens are a great way to keep your design system consistent and easy to maintain, they can be used across your entire application and can be used in your design tooling as well as your application. They are a great way to keep your brand consistent across all platforms and make it easy to maintain. 

In my opinion not implementing tokens is lazy and will cause you more issues in the long run. 

