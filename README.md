# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

1. What is the difference between an adaptive website and a fully responsive website?
An adaptive website combines a mix of both the old and the new; it applies media queries to establish breakpoints for different screen sizes, but still uses absolute units to define its layout. It's considered to still be too rigid for seamless use on any device. Fully responsive websites use percentage-based values for defining web layouts. This ensures that, whatever the screen size, the content adapts to the exact height and width of the viewport.

2. Describe what it means to be mobile first vs desktop first.
Mobile first and desktop first are two terms that refer to differing approaches to styling a website. Simply put, it refers to what version of the site is the default in styling. For example, with desktop first, all non-media queried styling is done for a large desktop-sized browser window. Conversely, mobile first means that the developers have made the mobile version of their website the default and that styling for tablet and desktop versions is delivered via media queries.
It should be noted that, now that mobile traffic accounts for more than 50% of all internet traffic, desktop first has been mostly deprecated. Google's algorithms also prioritize mobile-first layouts for their SEO. As such, most websites use mobile-first styling.

3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?
Usually, the default font-size for a browser is 16px. However, this makes using rem quite difficult because the developer has to continually keep track of what rem denotes in terms of pixels. However, 62.5% of 16 equals 10. Therefore, by setting `html` to `font-size: 62.5%`, 1`rem` is equal to `10px`, thus making the styling of fonts easier.

4. How would you describe preprocessing to someone new to CSS?
Preprocessing is somewhat like adding an extra layer on top of CSS, thereby giving you additional functionality that isn't incorporated in the normal version. A preprocessor takes a slightly-different version of CSS syntax, compiles it into JavaScript (where the extra functions are built), and then translates it back to normal CSS. This way, you can do cool stuff like nesting (styling multiple elements _inside_ one another), using mix-ins (CSS functions), and variables. You can also still use bog-standard CSS in LESS files, so it's incredibly versatile.

5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?
My favorite concept in preprocessing is the option to import other LESS files into another file. This makes the development process more organized, enabling you to style a specific module or section without having to deal with an enormous stylesheet that covers the entire site. It also negates the need for adding two dozen stylesheets into your HTML `<header>`, massively boosting performance, since all (imported) LESS files get compiled into a single LESS 'bundle' which gets served to the browser all at once.
The concept that still gives me the most trouble are mix-ins, especially ones with arguments. While I can see the the use, expecially when styling larger websites where the same button or element might occur hundreds of times in slightly-differing scenarios, I haven't really seen the use in our previous projects just yet. Therefore, the fact that mix-ins don't 'click' might have to do with a lack of use thus far.

You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Because you are using a preprocessor, there are two parts to setting up your project.  Be sure to run through the git set up first and then set up the preprocessor.

### Git Set up

Follow these steps to set up your project:

- [x] Create a forked copy of this project.
- [x] Add your project manager as collaborator on Github.
- [x] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [x] Create a new branch: git checkout -b `<firstName-lastName>`.
- [x] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [x] Push commits: git push origin `<firstName-lastName>`.
 
Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.
 

### Preprocessor Set up

* [x] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [x] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [x] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [x] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [x] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [x] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._  

### Home Page - Desktop HTML & LESS

* [x] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [x] Add a viewport meta tag to the head of your index.html page

* [x] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [x] Navigation Styles: Use the `navigation.less` file for styling.

* [ ] Main Content Styles: Use the `home-page.less` file for styling

* [ ] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [ ] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [ ]  Use at least 2 parameters to create your button

* [ ] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [ ] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [ ] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [ ] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription