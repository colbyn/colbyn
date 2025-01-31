# Biography & Status Timelines

## Pre 2025

[Overall very personal.]( PERSONAL-BIO.md )

**Some highlights are:**

- [Imager Project]( https://github.com/imager-io )
    Site performance tools for efficiently distributing media on the web. Notably includes a [tool]( https://github.com/imager-io/imager ) for optimizing the binary encoding of images in a brute force trial ’n error sorta manner, using a new (at that time) ML based perceptual quality metric designed to be a more accurate model of human perception compared to prior formulaic approaches. 
- My Note Taking Explorations:
    - The tools I developed to compile and publish my school notes such as,
        - [The HTML Toolchain]( https://github.com/subscript-publishing/subscript-html ) 
    - Also the notes themselves:
        - [colbyn's math notes]( https://colbyn.github.io/school-notes-spring-2020/ ).
            - Which I used to great effect and yet such left much to be desired, especially for hand drawn notes (see the following chem notes).
        - My proof-of-concept chemistry notes:
            - [root index]( https://colbyn.github.io/old-school-chem-notes/dev/chemistry-1010---fall-2021/index.html )
            - Where this differs from other note taking apps is its ability to support giant autogenerated **tables of contents** from the root notebook down to the individual pages.
            - [example page]( https://colbyn.github.io/old-school-chem-notes/dev/chemistry-1010---fall-2021/overview.html ).
    - Overall I wanted notes that were as compact as possible for any viewport resolution, and that could be navigated as quickly as possible in an obvious way.

## From 2025 onwards 

### [SuperSwiftMarkdownPrototype]( https://github.com/SuperSwiftMarkup/SuperSwiftMarkdownPrototype )

Initially the work began with a *proof-of-concept* prototype with the following aims: 
- Implement a native text renderer that supports all block types as defined in the GitHub Flavored Markdown Spec.
- With uniform behavior concerning text selection and selection-based navigation. Including: 
    - This includes the ability to select any inline text within any markdown block and be able to extend that selection across multiple and varying markdown block types. 
    - Cross platform support for multiple cursors / selections. 
- Implement all of the above without relying on macOS only APIs.
    - While the prototype was implemented in terms of AppKit APIs, the port to iOS should be relatively trivial. Especially since this project was itself based on an earlier codebase that was implemented in terms of UIKit and I have verified that the TextKit 2 functionality concerning text selections does indeed work on—at least—iOS 17 (which I honestly thought would be too good to be true lol). 

### [SuperSwiftMarkup]( https://github.com/SuperSwiftMarkup/SuperSwiftMarkup )

**At the time of this writing:**

Now that the core functionality has been proven viable, I (the author) have learned much and I intend to translate my experience and lessons learned from the *proof-of-concept* prototype codebase into a viable set of libraries that app developers can depend upon. Starting from a blank slate.

So keep in mind:
- This project is a complete rewrite from the ground up.
- The git tree is also a fresh start.
- At the time of this writing this project is in heavy development and does not yet present any cool tangible functionality.
- So head over to the aforementioned [*proof-of-concept* prototype](https://github.com/SuperSwiftMarkup/SuperSwiftMarkdownPrototype) to see the past history and screenshots from where that project left off (spoiler alert it’s super cool). 
- For the layperson, unless you’re interested in contributing towards or influencing the initial evolution of the SuperSwiftMarkup libraries, **please check back** every so often to see when some libraries therein are ready for real world use. 
- But if you’re interested in influencing the initial evolution of this project, then by all means dive in. 🙂


**High Level Objectives:**
- First class (cross platform) support for all markdown block types, with uniform behavior concerning text selection and selection-based navigation.
- First class (cross platform) support for multiple cursors/selections.
- Default support for everything under "Meeting the expectations of iOS and macOS users" (see [Appendix](#Appendix)).

**Additionally:**
- Where the rendering engine is designed in such a way that can accommodate,
    - Horizontally scrollable fragments (on a per-fragment basis) as an alternative to text wrapping. Which is particularly desirable for e.g. long tables that cannot neatly fit within their available view space.

**Overall I hope you’re excited as I am!** 

Personally I, the author (Colbyn Wadman), have been messing around with miscellaneous problems concerning text processing and text rendering (in one form or another) for a very long time and—as far as the POC has demonstrated—it’s good to see something interesting come from it, and when I release my work, I hope you’ll be pleased with the results. 🤞


# Links

## Dev Blogs

- [Medium]( https://medium.com/@colbyn )
- [SubStack]( https://colbynwadman.substack.com/ )

## Contact

- Email: hello@colbyn.com
