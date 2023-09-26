---
title: '🔥 Hot Take: If you''re not using Storybook you''re doing FE Development wrong'
description: 'A hot take on why you should be using Storybook for your next project'
pubDate: 'Sep 26 2023'
heroImage: '/codecult-placeholder.png'
---

Before we get to it, this is a heavily opinionated post so keep that in mind I like Storybook a lot so that should also be noted.

1. <a href="#why">Why</a>
2. <a href="#how">How</a>
3. <a href="#storybook-length">So you've heard "Storybook takes me longer to implement components." I'm here to say it does not.</a>
4. <a href="#">Autodocs</a>
5. <a href="#">Why would I not use Storybook?</a>
6. <a href="#">Summary</a>

## Why

Let's start at the beginning: what is Storybook, and why should I use it?

For those who have not had the chance to use Storybook before, it's incredibly easy to set up and takes little to no time. I won't go into the setup process here, as I'm covering that in a separate post along with some tips and tricks I normally use.

Storybook has recently implemented zero-config support for most CSS solutions, including:

- 💨 Tailwind
- 🧶 MaterialUI
- 💅 Styled Components
- 👩‍🎤 Emotion

But let's get back to what Storybook actually does and the problems it solves.

This is just a condensed version of the Storybook documentation, which is available here.

Over recent times, complexity with UIs and frontend development has been growing. Starting with responsive design, a typical component now has multiple factors to consider. For example, if you have a button that has 3 variants (with different background colors), you then have to check that variant on each modern browser (4). Additionally, you need to test this component on countless breakpoints. Managing all of this while ensuring no regression issues arise and all components work seamlessly becomes quite a headache.

Storybook Component Complexity

That's where Storybook bridges the gap. It can help you keep these variations and states in check across all browsers and breakpoints with some help from tools like Chromatic (also made by the Storybook team).

## How

In short, before my new blog post comes out, run the following command in the repository where you want to install Storybook:
npx storybook@latest init
And you're off to the races! It will ask some questions about your repository, so answer them correctly, and Storybook will be set up out of the box and ready to go.

For small plugins like the a11y plugin, which injects AXE accessibility tests into your stories, it's rather simple to add as well.

<h2 id="storybook-length">"Storybook takes me longer to implement components".</h2>

I've heard this complaint a lot. If your components are built in isolation and have data passed to them, you're primed to just copy and paste the same story over and over again. At the very least, with this approach, you get some documentation automatically generated, as well as all the extra bells and whistles that Storybook provides (a11y, testing, etc.).

This takes zero time. I mean, let's be real – the most you would do if you wanted a sleek-looking Storybook is to write your documentation alongside the code, for everyone to enjoy, instead of using Confluence or other external tools.

If you need some templates to steal, take a look at my ecommerce project that I'm building. I'm using Storybook extensively. At the time of writing, I haven't even touched Next.js. Instead, I'm building out each component before adding it to the main site.

## Autodocs

Autodocs are cool! Here's a link to a video explaining Autodocs. This feature allows you to write extensive documentation with almost zero effort – just copy and paste

Tell me why I'm wrong in the comments below. I'm releasing a new blog post about how I work with Storybook soon, so look out for that.

Why would I not use Storybook?
I'm not quite sure. Storybook has loads of benefits and can help create a robust, clean application. Not using it is pure insanity and inevitably leads to spaghetti code.

Summary
Hopefully, I've helped you see the light, and you'll choose Storybook for your next project. You'll get free documentation, regression testing, a11y testing, and interaction testing built-in with just around 10 minutes of effort for the setup.

🚀 Feel free to reach out if you have any questions or thoughts. Happy coding!