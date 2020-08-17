# cloud-hugo

Best Practices for Cloud Hosting of Hugo Static Sites

## Purpose

To provide best practices learned and earned through personal efforts in hosting of [Hugo](https://gohugo.io/) generated sites in the cloud.

Goals are not only baseline howto, but also how to set them up for automated deployment, as well as serve as collaborative publication pipelines for a group of authors to work on a site together, and to minimize the requirements of authors to know much of anything about Hugo.

## State of Play

Right now, as this repository of knowledge takes its baby steps, it will largely be focused around automated collaborative hosting in AWS.  That is the cloud provider I've been using for my efforts.  As time and testing allows, I'll be expanding these principles to other cloud providers and their tools.

## Assumptions

There is one assumption in all of this.  That the hosting options (of various levels of ease and capability) as described in [Hugo Documentation: Hosting & Deployment](https://gohugo.io/hosting-and-deployment/) are not a path you choose to take.

There are a number of ways to press an `Easy` button with Hugo publishing, to varying levels of ease, cost, and capability.  I personally chose to roll my own hosting, so I had complete control.  Additionally, were I to consider Hugo for enterprise-level usage, I'd likely be required to roll my own based on organizational or other constraints.

## Design Philosophy

In general, I focus on a few core fundamentals:

1. Focus on content, not formatting or technology.
2. Minimize knowledge hurdles to participation in authoring content.
3. Maximize collaboration via source control systems.
4. Enable **fast automated** publication pipelines to promote "living document" mindsets amongst authors.

These have grown out of my years in my career as an IT professional where I have served at times as technical writer and for many years as a business continuity author and coordinator.

These are the core elements of my approach in designing an environment that supports authors to publish to robust hosting solutions requiring little more than the subject-matter-expertise for which they are being asked to author documentation.

Hugo aligns well with Fundamental #1.  With minimal knowledge of website design, HTML, or other specialized knowledge, an author can create content without focusing on the design and delivery of that content.

However, Hugo alone struggles a little when considering Fundamentals #2 through #4.  That's where cloud, source controls, and a bit of integration automation come into play.

## Ideas & Goals

* **Diagramming capability.**
  * Want to add easy to use `Graphviz`, `Mermaid`, and/or `Draw.io` support.
  * Current integrations are add-on pipeline scripting around Hugo.
  * Or they are client-side processed `Mermaid`.
  * Need to find way to let Hugo handle `Mermaid` and `Graphviz` a bit more "natively" than is presently possible.
  * **Ideas**
    * **Fenced code blocks inside of Hugo shortcode block.**
      * **PRO** - Uses CommonMark standard Markdown.  Anything CommonMark-compliant should be able to parse the source Markdown files. Also leverages Hugo's templating engine capabilities.  And VS Code can interpret the fenced code block and display the diagram inline.  May not work for all editors, but it is a simple standard that meets with the Fundamentals.
      * **CON** - It's a tad messy.  It requires `exec()` capability in Hugo.
    * **Hugo Fork**
      * Fork exists.  See [jason-dour/hugo/tree/feature-exec](https://github.com/jason-dour/hugo/tree/feature-exec).
        * Initial working release. Use the shortcodes from [hugo/shortcodes](https://github.com/jason-dour/cloud-hugo/tree/master/hugo/shortcodes).
      * Also implements GV->SVG processing
      * Given the current state of conversation with Hugo developers, it is doubtful that a more generic exec framework is in the cards any time soon. I've attempted to [jumpstart the conversation](https://discourse.gohugo.io/t/the-long-overdue-need-for-converting-outputting-other-formats/27494/2).
* **In-memory Filesystem**
  * Could make Lambda processing instead of CodeBuild a very real possibility on larger sites.
  * Can possibly work if based in Python, but how can Hugo take advantage?
    * Possible to implement with a Hugo "wrapper" that first uses `afero` to unzip/untar/prepare your repo contents before setting Hugo loose?

## Examples

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
