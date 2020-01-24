# cloud-hugo

Best Practices for Cloud Hosting of Hugo Static Sites

## Purpose

To provide best practices learned and earned through personal efforts in hosting of [Hugo](https://gohugo.io/) generated sites in the cloud.

Goals are not only baseline howto, but also how to set them up for automated deployment, as well as serve as collaborative publication pipelines for a group of authors to work on a site together, and to minimize the requirements of authors to know much of anything about Hugo.

## State of Play

Right now, as this repository of knowledge takes its baby steps, it will largely be focused around automated collaborative hosting in AWS.  That is the cloud provider I've been using for my efforts.  As time and testing allows, I'll be expanding these principles to other cloud providers and their tools.

## Design Philosophy

In general, I focus on a few core fundamentals:

1. Focus on content, not formatting or technology.
2. Minimize knowledge hurdles to participation in authoring content.
3. Maximize collaboration via source control systems.
4. Enable **fast automated** publication pipelines to promote "living document" mindsets amongst authors.

These have grown out of my years in my career as an IT professional where I have served at times as technical writer and for many years as a business continuity author and coordinator.

These are the core elements of my approach in designing an environment that supports authors to publish to robust hosting solutions requiring little more than the subject-matter-expertise for which they are being asked to author documentation.

Hugo aligns well with Fundamental #1.  With minimal knowledge of website design, HTML, or other specialized knowledge, an author can create content without focusing on the design and delivery of that content.

However, Hugo struggles a little when considering Fundamentals #2 through #4.  That's where cloud, source controls, and a bit of integration automation come into play.

## Examples

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
